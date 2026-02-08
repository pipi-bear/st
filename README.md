# My st config (based on BreadOnPenguins/st)

This repo contains my personal st configuration.

Based on:
[BreadOnPenguins/st](https://github.com/BreadOnPenguins/st)

## Changes

### Additional patches

- clickurl (`st-clickurl-0.8.5.diff`)
- copyurl (`st-copyurl-multiline-20230406-211964d.diff`)
- desktopentry (`st-desktopentry-0.8.5.diff`)
- kitty-graphics (`st-kitty-graphics-20251230-0.9.3.diff`)

### Scope and notes

The adjustments in this repository are made **only for this forked setup** and are intended to resolve issues caused by the specific patch combination used here.

Note:
- The version from the official suckless repo does NOT have these issues.

Detailed description about my fix is as the following subsection.

### Fixes

Both the patch "copyurl" and "kitty-graphics" cause error when applying the `.diff` file to the forked version, due to:

- the member `line` is no longer in the `Term` structure from the forked version

A vanilla st cloned from the official suckless repo (`st 0.9.2`) is tested with `st-copyurl-multiline-20230406-211964d.diff`, and it works fine.

---
# Original README below
## simple terminal
  My very simple fork of st, comes with no guarantees or warranties <sub>(to be clear: this means things may not work as expected, or at all)</sub> :^)

## patches added
* alpha & changealpha (transparency)
* Xresources w/ reload signal (pywal takes priority)
* ligatures
* scrollback ringbuffer, with mouse
* anysize (ensures compatibility with various gaps setups in tiling WMs)

## other stuff
* If you aren't using ```~/.Xresources``` or [pywal](https://github.com/dylanaraps/pywal), default color palette is [Nord](https://www.nordtheme.com/).
* Read or change keybinds, default font/size, etc. in **config.h** - I'll update the man page at some point. Bindings are what you'd expect, besides:
  - ```alt + c``` & ```alt + v``` for copy-paste
  - ```alt + a``` & ```alt + s``` to increase and decrease alpha (transparency) respectively
  - ```alt + shift + k``` & ```alt + shift + j``` to increase and decrease font size, respectively

## how install pls?
```
git clone https://github.com/BreadOnPenguins/st
cd st
sudo make install
```
