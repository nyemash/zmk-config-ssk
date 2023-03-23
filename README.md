# zmk-config-ssk

## Notice
There might be the right way to do this but this works for me. Just learned ZMK, GitHub and KiCad to do this project in a short period of time so this might be pretty rough for those who know what they are doing. Had no intention to start this but had an extra n!n so why not.

## Description
Converting SSK to bluetooth by replacing the controller with a nice!nano v2 and a 595 shift register running on ZMK.

## Stuff
Gerber files below for JLCPCB but never had a chance to have this fabricated. Made some adjustments with this one based on the mistakes I learned from the prior version; which what I'm using. Adjustments were basically moving stuff around since parts were hitting the backplate. Might end up getting it done to have a cleaner build but I'm out of parts.

[Fab.zip](https://github.com/nyemash/zmk-config-ssk/files/11052187/Fab.zip)

Some pics.

Made the switch diagonal since the trace was wrong, removed the plastic housing on the battery connector since what I had in hand is a vertical one causing the LiPo connector interfer with the backplate and lastly clipped some of the excess solder on the nano since it was also hitting the backplate.
![image](https://user-images.githubusercontent.com/83567311/227261189-3442c988-3901-487a-ae98-6c2f759782df.png)

On/off where the pegs didn't fit the mounting hole.
![IMG_6562](https://user-images.githubusercontent.com/83567311/227259389-01cefa91-4113-45e8-a1d3-eea79b02a6fb.JPG)

## References/prior work
Made things easier.

* phosphorglow on DT: https://deskthority.net/viewtopic.php?t=8149
* iw0rm3r on GitHub:  https://github.com/qmk/qmk_firmware/blob/master/keyboards/converter/modelm101/readme.md
* Joe Scotto on YT: https://www.youtube.com/watch?v=O_urj-rF3bQ
* ZMK Discord
