# zmk-config-ssk

## Notice
There might be the right way to do this but this works for me. Learned ZMK, GitHub and KiCad to do this project for a short period of time so this might be pretty rough specially for those who know what they are doing. Had no intention to do this but had an extra nice!nano to try a wireless rotary so why not.

## Description
Bluetooth-ed my SSK by replacing the controller with a n!n v2 (21 pins) and a 595 shift register (8 pins but using 3 of the n!n) running on ZMK. You can do 22 pins for SSK (8R x 16C) but need to merge 2 columns with another 2 or if you want, drop another column then n!n would do fine.

## Stuff
Gerber files below for my 4th prototype - I'm completely done and might have been cheaper to go with FSSK. For this round, added diodes for the columns to have some sort of NKRO and prevent blocking; keys on the same row are blocking each other while pressed without the diodes. Only issue is that the "Right Alt" is triggering "Left" arrow when pressed. Luckily I don't use that Alt.     
~~Gerber files below for JLCPCB but never had a chance to have this fabricated. Made some adjustments with this one based on the mistakes I learned from the prior version; which what I'm using. Adjustments were basically moving stuff around since parts were hitting the backplate. Might end up getting it done to have a cleaner build but I'm out of parts.~~

[SSKoy.zip](https://github.com/nyemash/zmk-config-ssk/files/11471226/SSKoy.zip)

~~Pics and list on what I had to fix on my 2nd pcb / and going to 3rd. Need to try build a PCB again and add diodes per column to get some sort of key rollover but then ghosting would most likely occur.~~

* ~~Reset - reason for the slanted switch; to correct trace~~
* ~~Batt connector - used a vertical mount that interfered with backplate; use a horizontal female connector or move it up~~
* ~~Mounting hole securing the PCB by the two pegs - a little too high thus cannot flush pcb; had to drill it bigger; need to move it down a bit~~
* ~~MCU - interferes with backplate; don't use hotswap socket but need to raise it a bit to make room for the on/off switch (had to clip some solder to avoid contact) or move it up~~
* ~~PCB height - need allowance to let it slot in more easier to the case~~
* ~~Batt switch - pegs doesn't fit the PCB hole/connector; to correct the footprint~~

4th and final PCB
![IMG_6868](https://github.com/nyemash/zmk-config-ssk/assets/83567311/1a8457f1-0c78-45b1-ae8f-6649d1eec036)

As for the hotswap sockets, to clear the backplate of SSK go with the red one. I had to clip some of the bottom solder & pins on the n!n as well to make sure the pins doesn't touch. 
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
