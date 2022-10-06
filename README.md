# macbook_linux_scripts
Scripts to make linux functional on macbook pro 2017


########### brightness_control script ########
Adjust the brightness of the display
usage:  ./brightness_control [INC,DEC]


########### mouse_speed script ########
Increase the mount speed to .7, run on xstart

########### brcfmac43602-pci3.txt #######
Firmware for the broadcom wifi card.  Place in /lib/firmware/brcm and edit with correct mac address
This allows connection to 5g networks only.  
for non-5g networks: `sudo iwconfig wlp2s0 txpower 10dBm`

########### touchbar.sh ########
creates file /usr/local/bin/touchbar to change how the touchbar+fn key works
$ touchbar

########### network_suspend #######
stops NetworkManager and removes drivers for the wifi card before sleeping, still buggy after resume
goes in: /lib/systemd/system-sleep/

########### macbook-quirks.service #######
usbmuxd breaks touchbar functional, this service will fix it 
goes in: /etc/systemd/system/

########### Useful links #########
https://github.com/Dunedan/mbp-2016-linux (general state of macbook functionality)

https://github.com/davidjo/snd_hda_macbookpro (fix audio drivers)
https://github.com/davidjo/snd_hda_macbookpro/issues/63 (patched audio driver fix is above has compile errors) 
