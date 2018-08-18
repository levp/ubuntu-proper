# Ubuntu 14.04

## Install NVIDIA drivers

Remove any currently installed nvidia-related apps:  
`sudo apt-get purge nvidia*`

Install NVIDIA drivers version 346, other versions don't seem to work:
`sudo apt-get install nvidia-346`

## Disable Mouse Mcceleration

Check default acceleration/speed values:
`xset q | grep -A 1 Pointer`

Disable mouse acceleration:
`xset m 0/1 4` (values 1 and 4 could be different)

## Uninstall LibreOffice

```
sudo apt-get remove --purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove
```
## Disable Chrome "Middle Click to Lower Window" Behavior

`gsettings set org.gnome.desktop.wm.preferences action-middle-click-titlebar 'none'`

[source](https://askubuntu.com/a/655648)

