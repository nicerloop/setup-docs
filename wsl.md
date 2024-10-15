# Windows Subsystem for Linux (WSL)

[Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/windows/wsl) provides Linux environments integrated in Windows.

## Administrative install

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[Windows Subsystem for Linux](https://github.com/microsoft/WSL) can be installed using [WinGet](winget.md) and [gsudo](gsudo.md):

```shell
gsudo winget install Microsoft.WSL
```

:warning: :repeat: You may have to restart Windows to fully setup the newly enabled features. :repeat: :warning:

Run a first update as described hereafter to check for the latest kernel install.

## Administrative update

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[Windows Subsystem for Linux](https://github.com/microsoft/WSL) can be self updated using [gsudo](gsudo.md):

```shell
gsudo wsl --update
```

## Microsoft Store install

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[Windows Subsystem for Linux](https://github.com/microsoft/WSL) is available in the [Microsoft Store](https://apps.microsoft.com/) with ID [9P9TQF7MRM4R](https://apps.microsoft.com/detail/9P9TQF7MRM4R):

```shell
start ms-windows-store://pdp/?productid=9P9TQF7MRM4R
```
