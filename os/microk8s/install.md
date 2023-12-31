---
tags:
  - snapd
  - microk8s
  - kubernetes
  - kubectl
  - localstorage
---

# Install microk8s with snapd
```
sudo snap install microk8s --classic
```

# Basic permissions and settings
```
sudo usermod -a -G microk8s nullbr41n
sudo microk8s kubectl config view --raw > $HOME/.kube/config
sudo chown -R nullbr41n ~/.kube
newgrp microk8s
```

# Start/Status microk8s
```
microk8s start
microk8s status
```

# Get kubectl resources
```
microk8s kubectl get all -A
```

# microk8s install helm using snapd
```
sudo snap install helm --classic
```

# microk8s enable localstorage
`microk8s enable hostpath-storage`


# Working reference

py-image-dedup-k8s[https://github.com/nullbr41n/py-image-dedup-k8s]
