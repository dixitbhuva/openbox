
# OpenBox

Currently i am running debian 12


## Dependencies

- openbox
- pipewire
- brightnessctl
- playerctl

## Without Display Manager from tty1
add this to your **.xinitrc**
```bash
exec openbox-session
```
add this to **.bash_profile** or **.zprofile** for auto startx from tty1

```bash
if [ -z "$DISPLAY" ] && [ "$XDG_VTNR" = 1 ]; then
    exec startx
fi
```
- **startx:** means current tty1/shell don't replace by openbox, when you exit openbox you dont prompt for login in again
- **exec startx:** means your current shell is replaced with openbox, when you exit openbox you need to login again
- [Arch Wiki About Auto Startx](https://wiki.archlinux.org/title/Xinit#Autostart_X_at_login)

- may be i write more but this good at this time
