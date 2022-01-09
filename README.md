# DELL-G15-5510-ALCPlugFix
ALCPlugFix configuration for DELL G15 5510

Cetrain codecs need verb commands to be send when pluggin in headphones, and when waking up after sleep.
Seen on this DELL G15 5510 with ALC 295 there will be only a crackling sound without sending those verb commands. 
The config file for ALCPlugFix is included in this repostory.


| Info          | Detail        | Comment |
| ------------- | ------------- | ------- |
| Device        | Dell G15 5510 | |
| macOS         | Big Sur 11.6.2| |
| Method        | Vanilla       | |
| OpenCore      | 0.7.7         | |
| AppleALC Layout ID | 13 |       |
| Verb Command 1 | 0x19 SET_PIN_WIDGET_CONTROL 0x24 | Wakes up "Headset Mic Boost Volume", fixes the crackling sound. But no sound comes out of the headphones |
| Verb Command 2 | 0x1b SET_PIN_WIDGET_CONTROL 0x20 | Wakes up "Headphone Mic Boost Volume", makes sure there comes sound out the headphones |
| Verb Command 3 | 0x14 SET_PIN_WIDGET_CONTROL 0x40 | Wakes up ""Speaker Playback Switch" only needed after wake from sleep |


 ## Usage
To use [ALCPlugFix-Swift](https://github.com/black-dragon74/ALCPlugFix-Swift) you will need alcverbs=1 or alc-verbs added to be present under the HDEF device.

- Add alcverbs=1 bootarg or alc-verbs to the HDEF device
- Download [AlcPlugFix-Swift](https://github.com/black-dragon74/ALCPlugFix-Swift/) from [releases](https://github.com/black-dragon74/ALCPlugFix-Swift/releases)
- Unzip the file
- Open terminal
- cd ALCPugFix-Swift_directory 
- ./install.sh
- Select the [config file](https://github.com/TheHackGuy/DELL-G15-5510-ALCPlugFix/blob/main/DELL_G15_5510_ALC295.plist)
- Allow ALCPlugFix in System Preferences > Security & Privacy > General
- Give ALCPlugFix permissions System Preferences > Security & Privacy > Privacy > Full Disk Acces

## Credits
### ALCPlugFix-Swift
- [goodwin](https://github.com/goodwin) for original work on Obj-C based ALCPlugFix
- [zen-zhen](https://github.com/zhen-zen) for direct kernelspace connection
- [black-dragon74](https://github.com/black-dragon74) for writing and maintaing this software
