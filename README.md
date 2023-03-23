# zmk-config-ssk

## Notice
There might be the right way to do this but this works for me. Just learned ZMK, GitHub and KiCad to do this project in a short period of time so this might be pretty rough for those who know what they are doing. Had no intention to start this but had an extra n!n so why not.

## Description
Bluetooth-ed my SSK by replacing the controller with a nice!nano v2 (21 pins) and a 595 shift register (8 pins addional but using 3 if the n!n) running on ZMK.

## Stuff
Gerber files below for JLCPCB but never had a chance to have this fabricated. Made some adjustments with this one based on the mistakes I learned from the prior version; which what I'm using. Adjustments were basically moving stuff around since parts were hitting the backplate. Might end up getting it done to have a cleaner build but I'm out of parts.

... to add

Pics and list on what I had to fix on my 2nd pcb / for my 3rd.

* Reset - reason for the slanted switch; to correct trace
* Batt connector - vertical mount made it interfere with backplate; use a horizontal female connector or move it up
* Mounting hole securing the PCB by the two pegs - a little too high thus cannot flush pcb; had to drill it bigger; need to move it down a bit
* MCU - interferes with backplate; don't use hotswap socket (had to clip some solder to avoid contact) or move it up
* PCB height - need allowance to let it slot in more easier to the case
* Batt switch - pegs doesn't fit the PCB hole/connector; to correct the footprint

![image](https://user-images.githubusercontent.com/83567311/227261189-3442c988-3901-487a-ae98-6c2f759782df.png)

![IMG_6562](https://user-images.githubusercontent.com/83567311/227259389-01cefa91-4113-45e8-a1d3-eea79b02a6fb.JPG)

## References/prior work
Made things easier.

* phosphorglow on DT: https://deskthority.net/viewtopic.php?t=8149
* iw0rm3r on GitHub:  https://github.com/qmk/qmk_firmware/blob/master/keyboards/converter/modelm101/readme.md
* Joe Scotto on YT: https://www.youtube.com/watch?v=O_urj-rF3bQ
* ZMK Discord
