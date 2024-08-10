# NoSteamWebHelper
 A program that disables Steam's CEF/Chromium Embedded Framework.

## Aim
This program was created with the intent of replacing of Steam's command-line parameter `-no-browser` which was [removed.](https://steamcommunity.com/groups/SteamClientBeta/discussions/3/3710433479207750727/?ctp=42)


## How does NoSteamWebHelper kill or disable the CEF/Chromium Embedded Framework? 
- The executable does the following:
    - Launches Steam with the following arguments `-cef-single-process -cef-disable-breakpad -cef-disable-gpu-compositing` and appends any user provided ones, this restricts the CEF to a single process.
    - Injects the dynamic link library.

The dynamic link library toggles the CEF depending if an is app running or not.
- If an app is running then the CEF is disabled.
- If an app is not running then the CEF is enabled.

> [!NOTE]
> You may also manually toggle the CEF via a tray icon provided by NoSteamWebHelper.

This way, the Steam UI is still accessible to use.
    

# Build
1. hurrr durr double clike le sln
2. click le green build button on release
3. ??????
4. less bloated steam(pile of shite)