# Routing Game Audio to GoXLR Game

## Problem

Some Steam games (including Helldivers 2) do not expose an in-game audio device selector.
On Linux running games with Proton, this causes game audio to always go to the default sink, making it impossible to control via the GoXLR’s Game fader.


## Solution

After some digging around and consulting ChatGPT, I came up with the following solution. I was able to use **WirePlumber** stream rules to automatically route Proton/Wine audio streams to the GoXLR’s **Line 3** sink, which maps to the Game fader.

### Steps

1.  Identify the GoXLR Game sink

    List sinks:

    ```shell
    pactl list short sinks
    ```
    Typical GoXLR mapping:
    ```
    alsa_output.usb-TC-Helicon_GoXLR-00.HiFi__Line1__sink  ->  System
    alsa_output.usb-TC-Helicon_GoXLR-00.HiFi__Line2__sink  ->  Music
    alsa_output.usb-TC-Helicon_GoXLR-00.HiFi__Line3__sink  ->  Game
    ```

2.  Verify Proton game stream properties (one-time)

    Launch a Steam Proton game and inspect its stream:

    ```shell
    wpctl status
    wpctl inspect <stream-id>
    ```
    
    Here is an example for one of the three Helldivers 2 streams I had:

    ```
    > wpctl inspect 300 | egrep -i 'application\.name|application\.process|binary|media\.class|node\.name|pipewire\.id'
    
      * application.name = "HELLDIVERSï¿½ 2"
      application.process.binary = "wine64-preloader"
      application.process.host = "<host>"
      application.process.id = "20521"
      application.process.machine-id = "<machine-id>"
      application.process.session-id = "2"
      application.process.user = "<user>"
      * media.class = "Stream/Output/Audio"
      * node.name = "HELLDIVERSï¿½ 2"
    ```
    
    The relevant properties were:

    ```
    media.class = "Stream/Output/Audio"
    application.process.binary = "wine64-preloader"
    ```

3.  Create WirePlumber rule

    Create config directory:

    ```
    mkdir -p ~/.config/wireplumber/wireplumber.conf.d
    ```
    
    Create rule file:

    ```
    nano ~/.config/wireplumber/wireplumber.conf.d/51-proton-games-to-goxlr.conf
    ```

    Contents:
    
    ```
    monitor.stream-rules = [
      {
        matches = [
          { media.class = "Stream/Output/Audio", application.process.binary = "wine64-preloader" },
          { media.class = "Stream/Output/Audio", application.process.binary = "wine-preloader" }
        ]
        actions = {
          update-props = {
            node.target = "alsa_output.usb-TC-Helicon_GoXLR-00.HiFi__Line3__sink"
          }
        }
      }
    ]
    ```

    This matches Proton/Wine game audio only and routes it to the `GoXLR Game` fader.

4.  Restart audio stack (safe method)

    Always restart all `PipeWire` components together:
    ```
    systemctl --user restart pipewire pipewire-pulse wireplumber
    ```

5.  Verify

    Launch a Steam Proton game

    Open:

    ```
    pavucontrol
    ```
    
    Confirm the game stream is already routed to `GoXLR Game`.
    
    Move the `GoXLR Game` fader and hear if game audio levels are being changed.

### Notes / Caveats

This rule applies to all Wine/Proton audio, which is usually desirable for games.

If you run non-Steam Wine apps and want to exclude them, the rule can be further constrained (e.g. by matching steamapps in the command line).

Manual routing via `pavucontrol` always works as a fallback.
