---
tags:
  - arch linux
  - virtualenv
  - manjaro
  - pyenv


---


# Virtualenv with Arch Linux (manjaro)

```
# Clone pyenv
git clone https://github.com/pyenv/pyenv-virtualenv.git
cd pyenv-virtualenv
# Install pyenv
sudo ./install.sh
# Initialize
pyenv virtualenv-init -
```

# Running multiple/different version of python
```
#Run/Create pyenv with python version 3.9.0 under name of weirdAAL
pyenv virtualenv 3.9.0 weirdAAL

#activate pyenv
source /home/tikejhya/.pyenv/versions/3.9.0/envs/weirdAAL/bin/activate
