# zmk-config-ssk

## Notice
There might be the right way to do this but this works for me. Learned ZMK, GitHub and KiCad to do this project for a short period of time so this might be pretty rough specially for those who know what they are doing. Had no intention to do this but had an extra nice!nano to try a wireless rotary so why not.

## Description
Bluetooth-ed my SSK by replacing the controller with a n!n v2 (21 pins) and a 595 shift register (8 pins but using 3 of the n!n) running on ZMK. You can do 22 pins for SSK (8R x 16C) but need to merge 2 columns with another 2 or if you want, drop another column then n!n would do fine.

## Stuff
Gerber files below for my 4th prototype - I'm completely done and might have been cheaper to go with an FSSK then n!n. For this round, added diodes for the columns to have some sort of NKRO and prevent blocking; keys on the same row are blocking each other while pressed without the diodes. Now the only issue is that the "Right Alt" is triggering "Left" arrow when pressed. Luckily I don't use that Alt so I'll leave it as is.

[SSKoy.zip](https://github.com/nyemash/zmk-config-ssk/files/11471226/SSKoy.zip)

4th and final PCB
![IMG_6868](https://github.com/nyemash/zmk-config-ssk/assets/83567311/1a8457f1-0c78-45b1-ae8f-6649d1eec036)

For the hotswap pins & sockets, to clear the backplate of the SSK go with the red one. I had to clip some of the pins/solder on the bottom of the n!n as well to make sure there's no contact.
![IMG_6870](https://github.com/nyemash/zmk-config-ssk/assets/83567311/9c558f41-c355-4461-bb5c-57f3539b3115)

As for materials (some might not be the best selection, but had to work with what I already have)
1. nice!nano v2
2. 74HC595
3. https://sg.element14.com/amp-te-connectivity/5-520315-8/connector-ffc-fpc-8pos-2-54mm/dp/2890849
4. https://sg.element14.com/amp-te-connectivity/6-520315-6/conn-ffc-fpc-16pos-1row-2-54mm/dp/3791494
5. https://sg.element14.com/c-k-components/os102011ma1qn1/switch-spdt-0-1a-12v-pcb-r-a/dp/1201431
6. Mini 4-pin Push Button Switch
7. JST 2 Pin PCB header
8. 1N4148 Diodes
9. LiPo

## References & Guide
Made things easier.

* phosphorglow on DT - for matrix: https://deskthority.net/viewtopic.php?t=8149
* iw0rm3r on GitHub - for parts:  https://github.com/qmk/qmk_firmware/blob/master/keyboards/converter/modelm101/readme.md
* Joe Scotto on YT - excellent starter guide for building your own ZMK firmware: https://www.youtube.com/watch?v=O_urj-rF3bQ
* infinityis on GitHub - example of using 595 with n!n: https://github.com/customMK/zmk/tree/engikeeb/app/boards/shields/engikeeb
* ZMK Discord
