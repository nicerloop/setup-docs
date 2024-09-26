# Windows Subsystem for Linux (WSL)

[Windows Subsystem for Linux(WSL)](https://docs.microsoft.com/windows/wsl) provides Linux environments integrated in Windows.

## Administrative install

/!\ :name_badge: This requires elevated privileges /!\

[Windows Subsystem for Linux](https://github.com/microsoft/WSL) can be installed using [WinGet](winget.md) and [gsudo](gsudo.md):

```shell
gsudo winget install Microsoft.WSL
```

/!\ :repeat: You may have to restart Windows to fully setup the newly enabled features. /!\

Run a first update as described hereafter to check for the latest kernel install.

## Administrative update

/!\ :name_badge: This requires elevated privileges /!\

[Windows Subsystem for Linux](https://github.com/microsoft/WSL) can be self updated using [gsudo](gsudo.md):

```shell
gsudo wsl --update
```
