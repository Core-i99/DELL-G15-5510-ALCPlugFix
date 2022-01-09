# DELL-G15-5510-ALCPlugFix
ALCPlugFix configuration for DELL G15 5510

Cetrain codecs need verb commands to be send when pluggin in headphones, and when waking up after sleep.
Seen on this DELL G15 5510 with ALC 295 there will be only a crackling sound without sending those verb commands.

| Device | AppleALC Layout ID | Verb Command 1 | Verb Command 2 | Verb Command 3 |
| ------ | ------------------ | -------------- | -------------- | -------------- |
| Dell G15 5510 | 13 |        | 0x19 SET_PIN_WIDGET_CONTROL 0x24 | 0x1b SET_PIN_WIDGET_CONTROL 0x20 | ./alc-verb 0x14 SET_PIN_WIDGET_CONTROL 0x40 |
