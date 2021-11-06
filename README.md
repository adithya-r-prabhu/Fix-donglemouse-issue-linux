# Fix-donglemouse-issue-linux


    sudo modprobe -r usbhid && sudo modprobe -r psmouse
    sudo modprobe usbhid && sudo modprobe psmouse

to run this at startup create a bash scipt containing :

#bin/bash
sudo modprobe -r usbhid && sudo modprobe -r psmouse
sudo modprobe usbhid && sudo modprobe psmouse
echo "mouse is reset "
echo "task end"

to any directory and save as filename.sh

then run 

    crontab -e

in terminal.

then add 

    @reboot /path/to/script

to the file and save 
