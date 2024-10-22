# VirtualBox

[VirtualBox](https://www.virtualbox.org/) is a virtualization solution.

## Standard install

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[VirtualBox](https://www.virtualbox.org/) requires [Microsoft Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) which can be installed using [WinGet](winget.md) and [gsudo](gsudo.md): 

```shell
gsudo winget install Microsoft.VCRedist.2015+.x64
```

[VirtualBox](https://www.virtualbox.org/) can be installed using [WinGet](winget.md) and [gsudo](gsudo.md):

```shell
gsudo winget install Oracle.VirtualBox
```

### Specific version

If a [specific version](https://www.virtualbox.org/wiki/Download_Old_Builds) is required, for example for compatibility with [Vagrant](vagrant.md), the version parameter can be specified:


```shell
gsudo winget install Oracle.VirtualBox -v 7.0.20
```

The list of available versions can be found on [winstall.app](https://winstall.app/apps/Oracle.VirtualBox)
