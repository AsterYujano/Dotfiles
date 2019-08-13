# Dotfiles

## Firefox _Developper Edition_

Dark theme, density normal or compact

### Extensions

- Invidition: Youtube tracking protection + bypass proxy restrictions at working place
- Ublock Origin
- Privacy Badger
- HTTPS everywhere
- Vimium
- Momentum (fancy but cool)
- Duckduckgo privacy essentials
- Grammarly

### Install

https://zillowtech.com/install-firefox-developer-edition-linux.html

## Wallpaper

```
mkdir ~/Pictures/wallpapers
cd ~/Pictures/wallpapers
wget http://hdqwalls.com/wallpapers/small-memory-lp.jpg
```

With i3, add at the end of the `~/.config/i3/config` file the `feh` wallpaper line

## Screen brightness

```
sudo find /sys/ -type f -iname '*brightness*'

# to change with correct card
sudo ln -s /sys/devices/pci0000:00/0000:00:02.0/drm/card0/card0-LVDS-1/intel_backlight  /sys/class/backlight
```

```
sudo nano /etc/X11/xorg.conf



  Section "Device"
        Identifier  "Intel Graphics" 
        Driver      "intel"
        Option      "Backlight"  "intel_backlight"
    EndSection

```

try `xbacklight -inc 20` (so install xbacklight)

## Syncthing & KeepassXC

Install [Syncthing](https://syncthing.net/)
```
sudo dnf install syncthing-gtk
```

Install [KeepassXC](https://keepassxc.org/)
```
sudo dnf install keepassxc
```

## File Manager

Thunar is pretty simple and handle mount/unmount of USB sticks & SD card

```
sudo dnf install thunar
```

## Font

```
sudo dnf install lxappearance
```
launch it, then change font with smth like Sans

## SSH keys

install xclip (pretty useful)

```
# generate keys (if needed), check for it before : ~/.ssh/HERE
ssh-keygen -t rsa -b 4096 -C "EMAIL_ADRESS"

# copy the key
xclip -sel clip < ~/.ssh/id_rsa.pub
```
