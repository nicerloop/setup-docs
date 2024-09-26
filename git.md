# git

[git](https://git-scm.com) is a source code management tool.

## Standard install

[git](https://git-scm.com) can be installed using [Scoop](scoop.md):

```shell
scoop install main/git
```

## Fix: `warning: [...]: Filename too long`

From https://stackoverflow.com/a/22575737

1. Enable long paths in Windows 10

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" -Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force
```

2. Enable long paths in Git

```shell
git config --system core.longpaths true
```
