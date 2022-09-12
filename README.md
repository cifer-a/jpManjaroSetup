# jpManjaroSetup
How to set up Manjaro linux with japanese keyboard



1. Go to manjaro.org and select the KDE image

The japanese keyboard settings only work well with the KDE desktop manager (how the user interface looks) at the time of this writing.

2. Burn the ISO file to a USB drive

2.1 Figure out how to boot from USB on the device you use
2.2 Insert the USB drive and boot from it
// Try the "proprietary drivers" version if default does not work
2.4 before initiating the installation, make sure that you can connect to the wifi
2.5 if you cannot connect to the wifi, you may want to try the full image if you selected the minimal image
2.6 if the wifi does not work with the full image, you will want to research how to get it to work, and perhaps succeed in the live version 
2.7 if you cannot get the wifi to work, avoid installing unless wifi is unnecessary

3. Install linux on the device

## Setting up the keyboard

4. Install packages fcitx5 fcitx5-im fcitx5-mozc

5. enter "fcitx5-configtool"

6. add japanese (latin letters) and mozc to the group

Avoid adding more than one group, as the Japanese letters only will work in the system applications then.
I.e., in order to get hiragana/romaji functionality to work in the browser and office editors, only one group can be used.

7. set up config: 
> nano ~/.pam_environment

In the editor, add the following:
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx

then exit and save: press ctrl+x (exit the nano editor) and "y" to save

8. Maybe it will suffice to log out and back in, if not try to reboot.

// check here for more, or search for fcitx5 + japanese on the web 
https://wiki.archlinux.org/title/Fcitx5
