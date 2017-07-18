# RadioManager Bash client

[![Snap Status](https://build.snapcraft.io/badge/Pluxbox/radiomanager-cli.svg)](https://build.snapcraft.io/user/Pluxbox/radiomanager-cli)

## Overview
This is a Bash client script for accessing RadioManager service.

The script uses cURL underneath for making all REST calls.

To get started using RadioManager-cli, please install snapd using the commands provided for your distro.

# Install
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

# Usage
Once installed, you can get started using radiomanager-cli.

```shell
# Print the list of operations available on the service
$ radiomanager-cli -h

# Print the service description
$ radiomanager-cli --about

# Print detailed information about specific operation
$ radiomanager-cli <operationId> -h

# Make GET request
$ radiomanager-cli --host http://<hostname>:<port> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make GET request using arbitrary curl options (must be passed before <operationId>) to an SSL service using username:password
$ radiomanager-cli -k -sS --tlsv1.2 --host https://<hostname> -u <user>:<password> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make POST request
$ echo '<body_content>' | radiomanager-cli --host <hostname> --content-type json <operationId> -

# Make POST request with simple JSON content, e.g.:
# {
#   "key1": "value1",
#   "key2": "value2",
#   "key3": 23
# }
$ echo '<body_content>' | radiomanager-cli --host <hostname> --content-type json <operationId> key1==value1 key2=value2 key3:=23 -

# Preview the cURL command without actually executing it
$ radiomanager-cli --host http://<hostname>:<port> --dry-run <operationid>

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
