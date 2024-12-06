# WinGet

[WinGet](https://github.com/microsoft/winget-cli) is the Windows Package Manager.

## Windows 11

[WinGet](https://github.com/microsoft/winget-cli) is present in standard Windows 11 installations and does not need to be installed.

## Standard  install

[WinGet](https://github.com/microsoft/winget-cli) can be installed with [Scoop](scoop.md):

```shell
scoop install main/winget
```

## Package discovery

Many packages are available through [WinGet](https://github.com/microsoft/winget-cli).
You can browse and search the package repository from the third-party site:

* [winstall](https://winstall.app)
* [wingetCollections](https://winget.ragerworks.com/)

## Package update

You can upgrade all packages installed in user scope:

```shell
winget upgrade --all
```
