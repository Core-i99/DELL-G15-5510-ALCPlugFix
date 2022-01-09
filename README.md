# DELL-G15-5510-ALCPlugFix
ALCPlugFix configuration for DELL G15 5510

Cetrain codecs need verb commands to be send when pluggin in headphones, and when waking up after sleep.
Seen on this DELL G15 5510 with ALC 295 there will be only a crackling sound without sending those verb commands.

| Info          | Detail        |
| ------------- | ------------- |
| Device        | Dell G15 5510 |
| macOS         | Big Sur 11.6.2|
| Method        | Vanilla       |
| OpenCore      | 0.7.7         |
| AppleALC Layout ID | 13 |
| Verb Command 1 | 0x19 SET_PIN_WIDGET_CONTROL 0x24 |
| Verb Command 2 | 0x1b SET_PIN_WIDGET_CONTROL 0x20 |
| Verb Command 3 | 0x14 SET_PIN_WIDGET_CONTROL 0x40 |
