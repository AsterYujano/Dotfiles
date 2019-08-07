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

try `xbacklight -inc 20`
