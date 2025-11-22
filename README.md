# Hyprland-based desktop configuration bundle

Building blocks of a standalone desktop environment.

Created and tested on an Ach+KDE based system. For personal use; Wholly unsuited for broad application.

## Components

- `Hyprland`
- `Waybar`
- `Matugen`
- `SWW`
- `Rofi`
- `SwayNotificationCenter`
- `Equinox`
- bespoke scripts - theme switcher/generator etc.

## Instructions

### Theme swapper

`hyprland-theme-swapper` coordinates automatic theme switching by picking a wallpaper, generating a new matugen scheme and updating all the individual components' themes. To make it work:

- make sure its dependencies are resolved (`babashka deps` etc. check the repo's readme)
- make sure its executable and on PATH, for example:
```sh
# File:  ~/.local/bin/hypr-swap-theme
#!/bin/sh
/bin/env bb ~/.local/lib/hypr-theme-swapper/theme_swapper.clj $@
```
