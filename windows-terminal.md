# Windows Terminal

[Windows Terminal](https://github.com/microsoft/terminal) is the new Windows Terminal from Microsoft.

## Windows 11

`Windows Terminal` is the default terminal for Windows 11 and does not need to be installed.

## Scoop install (portable app)

[Windows Terminal](https://github.com/microsoft/terminal) can be installed using [Scoop](scoop.md):

```shell
scoop bucket add extras
scoop install windows-terminal
```

`Windows Terminal` can be registered in Windows Explorer:

```shell
reg import $HOME\scoop\apps\windows-terminal\current\install-context.reg
```

and unregistered before uninstall:

```shell
reg import $HOME\scoop\apps\windows-terminal\current\uninstall-context.reg
```

## WinGet install (packaged app)

[Windows Terminal](https://github.com/microsoft/terminal) can be installed using [WinGet](winget.md):

```shell
winget install Microsoft.WindowsTerminal
```

When installed , `Windows Terminal` can be selected as the default terminal:

* Start Menu
* Settings
* Update and Security
* Developer
* Terminal
