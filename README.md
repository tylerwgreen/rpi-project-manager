# Raspberry Pi Project Manager

Raspbian Jessie

## Setup

### Desktop Icons

[How To](http://www.raspberry-projects.com/pi/pi-operating-systems/raspbian/gui/desktop-shortcuts)

Create symbolic links

```
ls -s ~/saguaro-man/desktop/name-of-file.desktop ~/Desktop/name-of-file.desktop
```

### Auto Start & Disable Screen Saver

[How To](https://www.raspberrypi.org/forums/viewtopic.php?f=91&t=163316)

```
vim ~/.config/lxsession/LXDE-pi/autostart
```

Update to:

```
@lxpanel --profile LXDE-pi
@pcmanfm --desktop --profile LXDE-pi
@xscreensaver -no-splash # comment this line out to disable screensaver
@xset s off
@xset -dpms
@xset s noblank
bash /home/pi/projects/rpi-project-manager/bin/startup
```

### Remove Bloatware

[How To A](http://raspi.tv/2016/how-to-free-up-some-space-on-your-raspbian-sd-card-remove-wolfram-libreoffice)

[How To B](https://project.altservice.com/issues/418)

```
sudo apt-get remove --purge wolfram-engine libreoffice* penguinspuzzle
sudo apt-get autoremove
sudo apt-get clean
rm -rf /home/pi/python_games
```

## Notes

Projector resolution: 1280x800
Display resoultion: 800x480
