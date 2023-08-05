# Install snapd

Snapd: The snap daemon; it's the background service that manages and maintains the snaps on a (Arch) Linux system.

```
git clone https://aur.archlinux.org/snapd.git
cd snapd
makepkg -si
```

## Enable snapd
```
sudo systemctl enable --now snapd.socket
```

# symlink as snap
```
sudo ln -s /var/lib/snapd/snap /snap
