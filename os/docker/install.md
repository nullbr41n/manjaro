---
tags:
  - arch linux
  - manjaro
  - docker
  - systemctl
---

# Installing docker in Arch Linux

```
https://docs.docker.com/desktop/release-notes/
sudo pacman -U ~/data/docker-desktop-4.21.1-x86_64.pkg.tar.zst
```

# Enabling docker with systemctl
```
systemctl --user start docker-desktop
systemctl --user enable docker-desktop
