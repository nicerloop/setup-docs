# WinGet

[WinGet](https://github.com/microsoft/winget-cli) is the Windows Package Manager.

## Standard  install

[WinGet](https://github.com/microsoft/winget-cli) can be installed with [Scoop](scoop.md):

```shell
scoop install main/winget
```

## Package discovery

Many packages are available through [WinGet](https://github.com/microsoft/winget-cli).
You can browse and search the package repository from the third-party [winstall](https://winstall.app) site.

## Package update

You can upgrade all packages installed in user scope:

```shell
winget upgrade --all
```
