## Related Repository

- https://github.com/nagadomi/cutorch
- https://github.com/nagadomi/cunn
- https://github.com/nagadomi/cudnn.torch

## Original README.md

[![Build Status](https://travis-ci.org/torch/distro.svg?branch=master)](https://travis-ci.org/torch/distro)

#### NOTE: Torch is not actively developed anymore and is in maintenance mode.

Self-contained Torch installation
============

#### Please refer to the [Torch installation guide](http://torch.ch/docs/getting-started.html#_) for details on how to make a fresh install of Torch on Linux or MacOS.
#### If on windows with msvc, please refer to this [guide](win-files/README.md) for details on installation and usage.


## Repo content
#### Dependencies
Globally installed dependencies can be installed via:
```bash
sudo bash install-deps
```

#### Lua and Torch
The self-contained Lua and Torch installations are performed via:
```bash
sudo ./install.sh
```

By default Torch will install LuaJIT 2.1. If you want other options, you can use the command:
```bash
# If a different version was installed, used ./clean.sh to clean it
TORCH_LUA_VERSION=LUA51 ./install.sh
TORCH_LUA_VERSION=LUA52 ./install.sh
```

Finally make sure to properly setup access rights:
```bash
sudo chown -R install
sudo chown -R build
```

## Update
To update your already installed distro to the latest `master` branch of `torch/distro` simply run:
```bash
sudo ./update.sh
```

## Cleaning
To remove all the temporary compilation files you can run:
```bash
sudo ./clean.sh
```

To remove the installation run:
```bash
# Warning: this will remove your current installation
sudo rm -rf ./install
```
You may also want to remove the `torch-activate` entry from your shell start-up script (`~/.bashrc` or `~/.profile`).

## Test
You can test that all libraries are installed properly by running:
```bash
./test.sh
```

Tested on Ubuntu 14.04, CentOS/RHEL 6.3 and OSX
