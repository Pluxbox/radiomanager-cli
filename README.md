# RadioManager Bash client

[![Snap Status](https://build.snapcraft.io/badge/Pluxbox/radiomanager-cli.svg)](https://build.snapcraft.io/user/Pluxbox/radiomanager-cli)

## Overview
This is a Bash client script for accessing RadioManager service.

The script uses cURL underneath for making all REST calls.

To get started using RadioManager-cli, please install snapd using the commands provided for your distro.

## Install
## Ubuntu/Debian/Mint

```shell
sudo apt install snapd
sudo snap install radiomanager-cli
```

## Redhat/Fedora/CentOS

```shell
sudo dnf install snapd
sudo systemctl enable --now snapd.socket
sudo snap install radiomanager-cli
```

## ARCH

```shell
sudo pacman -S snapd
sudo systemctl enable --now snapd.socket
sudo snap install radiomanager-cli
```

## OpenSUSE

For 42.2:
```shell
sudo zypper addrepo http://download.opensuse.org/repositories/system:/snappy/openSUSE_Leap_42.2/ snappy
```
For Tumbleweed:
```shell
sudo zypper addrepo http://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed/ snappy
```
You can then install snapd and radiomanager-cli:
```shell
sudo zypper install snapd
sudo snap install radiomanager-cli
```

## Docker image
You can easily create a Docker image containing a preconfigured environment
for using the REST Bash client including working autocompletion and short
welcome message with basic instructions, using the generated Dockerfile:

```shell
docker build -t my-rest-client .
docker run -it my-rest-client
```

By default you will be logged into a Zsh environment which has much more
advanced auto completion, but you can switch to Bash, where basic autocompletion
is also available.

## Shell completion

### Bash
The generated bash-completion script can be either directly loaded to the current Bash session using:

```shell
source radiomanager-cli.bash-completion
```

Alternatively, the script can be copied to the `/etc/bash-completion.d` (or on OSX with Homebrew to `/usr/local/etc/bash-completion.d`):

```shell
sudo cp radiomanager-cli.bash-completion /etc/bash-completion.d/radiomanager-cli
```

#### OS X
On OSX you might need to install bash-completion using Homebrew:
```shell
brew install bash-completion
```
and add the following to the `~/.bashrc`:

```shell
if [ -f $(brew --prefix)/etc/bash_completion ]; then
  . $(brew --prefix)/etc/bash_completion
fi
```

### Zsh
In Zsh, the generated `_radiomanager-cli` Zsh completion file must be copied to one of the folders under `$FPATH` variable.
