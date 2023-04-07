# Hackintosh the ThinkPad X13 Gen1

<p align="center">
    <a href="https://www.apple.com/macos/ventura/">
        <img src="https://img.shields.io/badge/macOS-Ventura_13.2-orange.svg"/>
    </a>
    <a href="https://github.com/acidanthera/OpenCorePkg">
        <img src="https://img.shields.io/badge/OpenCore-0.9.1-blue.svg"/>
    </a>
</p>

# Contect

- Intro
- Disclaimer
- Devices
- Work/Issues/Not Work
- Before / After Installation
- Other Respositories
- Credits

# Intro

This includes an EFI(Opencore) which works on Hackintosh the ThinkPad X13 Gen1

# Disclaimer

Your warranty is now void. Please do some research if you have any concerns before utilizing my project. I am not responsible for any loss, including but not limited to Kernel Panic, device fail to boot or can not function normally, storage damage or data loss, atomic bombing, World War III, The CK-Class Restructuring Scenario that SCP Foundation can not prevent, and so on.

# Devices

| Category  | Component                                       | Note                                                         |
| --------- | ----------------------------------------------- | ------------------------------------------------------------ |
| Type | 20T2 | - |
| CPU | Intel Core i7-10510U | - |
| GPU | Intel UHD Graphics 620| - |
| SSD | Intel HBRPEKNX0202AL(Intel® Optane™) 512GB| HackIONVMeFamily.aml is used to patch SSDs with Intel Optane™, which can cause Crash.If you replace the SSD, please to remove ACIP\HackIONVMeFamily.aml|
| Screen | 14" FHD - 1920 x 1080 | - |
| Memory | 16GB / 2133MHz LPDDR4 | - |
| Battery | Integrated Li-Polymer 51Wh Maybe? | - |
| Camera | 720p Camera | - |
| Wi-Fi & BT | Intel Wi-Fi 6 AX201 | - |
| Input | PS2 Keyboard & Synaptics I2C HID TrackPad | - |
| Ports | 1 x USB TB3 /1 x USB3 Type-C/2 x USB 3| - |
| Audio | Realtek ALC257 Maybe? |

# Working ✅
| Feature | Notes |
| --------- | ----------------------------------------------- | 
| Screen 🖥 | ✅ |
| Keyboard/TouchPad/Track Point⌨️| ✅ |
| ThunderBlot 3 hot plugging | ✅ , Tested Thunderbolt 3 port, connected TB3 hub,video output 2k/SSD/audio output, I'm not sure if others are available|
| USB-A / USB-C | ✅|
| Speaker/Hadphone jack 🔉| ✅ |
| Video Output | ✅ ,HDMI/USB-C/TB3 |
| Sleep 🛏️ | ✅ |
| F1-F3🔊,F5-F6🌞 Keys|✅|
| Internal Camera|✅|
| Handoff |✅|

# Known Issues ❓
| Feature | Notes |
| --------- | ----------------------------------------------- |
| Wireless | ❓,When installing macOS, there is no stable wireless network driver so far, so it is recommended to use wired network(USB network card) during installation.|
| SD Card Reader| ❓,I didn't test it, I don't know if it work|
| Battery | ❓,I didn't patching it deeply, it should work|

# Not Working ❌
| Feature | Notes |
| --------- | ----------------------------------------------- |
| Internal microphone|❌,No workaround to get Intel® SST working yet|
| Apple Music Lossless / Apple TV / Disney+ |❌,DRM is broken for iGPU-only systems|
| Finger Reader|❌,Impossible|
| F4,F7-F12 keys|❌,No fix plan|
| AirDrop, Apple Watch unlock ,|❌,Intel network card support not yet|

# Before Install
- Generate new SMBIOS https://github.com/corpnewt/GenSMBIOS
- The current wireless driver is not very stable, you may need to prepare a wired network (or try to add a wireless network manually during the installation)

# After Install
- Setting > TouchPad. Untick Force Click and haptic feedback this one causing invert click on touchpad
- Download [HelPort](https://github.com/zxystd/HeliPort) for a stable wireless network experience

# Other Respositories

- x1c6-hackintosh <https://github.com/tylernguyen/x1c6-hackintosh>
- ThinkPad-X1C8-Hackintosh <https://github.com/HJebbour/ThinkPad-X1C8-Hackintosh>
- Lenovo-Y900x-Hackintosh <https://github.com/SukkaW/Lenovo-Y9000X-Hackintosh>

# Credits

- The guys from [Acidanthera](https://github.com/acidanthera) that make this possible
- [Apple](http://apple.com) for macOS
- Thanks to [Tylernguyen](https://github.com/tylernguyen/) for the thunderbolt 3 hot-plug ACPI files
- Intel Optane drive patch,thanks to the tutorial(Chinese) by "一直幸运一直作死",https://zhuanlan.zhihu.com/p/429073173
