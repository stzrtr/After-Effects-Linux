# Run Adobe After Effects on Linux
Literally as the title said.\
Special thanks to [@unable2access](https://github.com/unable2access) for helping me A LOT, also shout out to [this](https://github.com/relativemodder/aegnux) repository for setting up things that are simply "I'm too lazy to do it" type shi- /hj

## Current supported versions
|  After Effects version  |  Wine version  |  Installs properly  |  Workarounds  |  Runs properly  |
| :--- | :--- | :--- | :--- | :--- |
|  CC 2014  |  wine-11.7  |  Yes  |  Turn internet off during installation  |  ☑️ Works properly with font error spam and index error spam after splash screen, motion blur not working  |
|  CC 2015.3  |  wine-11.7  |  Yes  |  Turn internet off during installation  |  ☑️ Works properly with font error spam and index error spam after splash screen
|  CC 2018  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |
|  CC 2019  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |
|  CC 2020 (18.0)  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, stuck on "Initializing MediaCore..."  |
|  CC 2021  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, crash after splash screen   |
|  CC 2022  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, crash after splash screen   |
|  CC 2023  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, crash after splash screen   |
|  CC 2024  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, launches after splash screen but no preview (can't render)   |
|  CC 2025  |  wine-11.7  |  Yes  |  None  |  ❎ Not working, crash during loading   |
|  CC 2026  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |  _not yet tested_  |

## Current test bench
**Lenovo ThinkPad T14 Gen 1 (AMD)** - [@stzrtr](https://github.com/stzrtr)
- OS: Arch Linux x86_64
- Kernel: Linux 6.19.14-zen1-1-zen
- CPU: AMD Ryzen 5 PRO 4650U (12)
- GPU: AMD Radeon Vega Series / Radeon Vega Mobile Series [Integrated]
- Wine version: 11.7 stable

## How to install
### Prerequisites
- Same as Adobe's minimum system requirements (64-bit system, blablablah), I bet any Linux distro will work as intended.
- Latest version of `wine` is recommended!
- Your time to do all of these.
### Disclaimer
This by any means are not meant to be a Windows/macOS replacement as what Adobe is natively runs on, I do this for fun and I believe Adobe _should_ consider the Linux version of their programs.
> Of course it's merely impossible from a capitalist corporate who took subscriptions like a contract between someone's relationship who didn't make it lol

Okay, enough ranting. Let's get back on track!

### Steps
1. Install `wine` and `winetricks`, in my case it's `pacman -S [package]`
```
  $ sudo pacman -S wine
  $ sudo pacman -S winetricks
```
2. Install After Effects \
   You might want to boot into Windows (or Windows's VM) to install if it fails to install via `wine`
3. Once installed, make sure that:
   - `autohotkey` is installed via `winetricks` for keyboard shortcuts, on KDE or Ubuntu's GNOME you might encounter `Ctrl+Alt+T` keybinds as open Terminal instead of time remapping so you need to remap in After Effects itself.
   - Some optional prefixes like `graphics=wayland, renderer=vulkan, sound=alsa, videomemorysize=2048, win10`
4. Optional: If you'd like to install extension(s) that requires changing registry/ies, use `winetricks` to apply!
5. Test run, if it works then enjoy!

## What's next?
Yes, I need more testers with different specs... I daily drive AMD (CPU & GPU) as for now so I need someone who has Intel and NVIDIA combo, also pretty much welcome for any changes.\
I might not properly maintain this repository as I'm busy with uni chores. 😓
