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

# Gotcha

- error retrieving subordinate uid range


If `/etc/subuid` and `/etc/subgid` are missing, they need to be created.
Both should contain entries in the form -
`<username>:<start of id range>:<id range size>`. For example, to allow the current user
to use IDs from 100000 to 165535:

```console
$ grep "$USER" /etc/subuid >> /dev/null 2&>1 || (echo "$USER:100000:65536" | sudo tee -a /etc/subuid)
$ grep "$USER" /etc/subgid >> /dev/null 2&>1 || (echo "$USER:100000:65536" | sudo tee -a /etc/subgid)
```

To verify the configs have been created correctly, inspect their contents:

```console
$ echo $USER
exampleuser
$ cat /etc/subuid
exampleuser:100000:65536
$ cat /etc/subgid
exampleuser:100000:65536
```
