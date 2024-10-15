# Ubuntu

[Ubuntu](https://ubuntu.com/desktop/wsl) is a Linux distribution.

It requires [Windows Subsystem for Linux (WSL)](wsl.md) to run seamlessly in Windows.

## Standard install

[Ubuntu](https://ubuntu.com/desktop/wsl) can be installed using [WinGet](winget.md):

```shell
winget install Canonical.Ubuntu.2204
```

## Default configuration

Launch `ubuntu` once to trigger the first-run setup procedure:

```powershell
& "$HOME\AppData\Local\Microsoft\WindowsApps\ubuntu.exe"
```

Fill in the WSL Ubuntu username and password, for example:

* username: `wsluser`
* password: `password`

Quit Ubuntu shell:

```bash
exit
```

### Configure default WSL distribution

Set Ubuntu as the default WSL distribution:

```shell
wsl -s Ubuntu
```

### Optional: Configure HTTP proxy

Define `http_proxy`and `https_proxy` environment variables in `$HOME/.bash_aliases` file, which is sourced by `$HOME/.bashrc` :

`\\wsl.localhost\Ubuntu\home\<wsluser>\.bash_aliases`

```bash
export http_proxy="http://<hostname>:<port>"
export https_proxy="${http_proxy}"
```

### Optional: Configure local Px HTTP proxy

Configure the HTTP proxy as described above, with the [Px](px.md) configuration as seen from WSL:

```bash
export http_proxy="http://$(hostname).local:3128"
```

## Update WSL Ubuntu packages

Jump inside WSL Ubuntu, elevate to root and update packages using `apt`:

```bash
wsl
sudo -i --preserve-env=http_proxy,https_proxy
apt update
apt upgrade -y
exit
exit
```

## Microsoft Store install

[Ubuntu](https://ubuntu.com/desktop/wsl) is available in the [Microsoft Store](https://apps.microsoft.com/) with ID  [9PDXGNCFSCZV](https://apps.microsoft.com/detail/9PDXGNCFSCZV):

```shell
start ms-windows-store://pdp/?productid=9PDXGNCFSCZV
```
