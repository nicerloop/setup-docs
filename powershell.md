# PowerShell

[PowerShell](https://github.com/PowerShell/PowerShell) is a cross-platform command-line shell and scripting language for Windows, Linux, and macOS.

[Windows PowerShell 5.1](https://learn.microsoft.com/en-us/powershell/scripting/whats-new/differences-from-windows-powershell
) is an integral part of and is available only on Windows. [PowerShell](https://github.com/PowerShell/PowerShell) 6 and later is distributed as a standalone product for Windows, macOS, and Linux.

## Standard install

Install [PowerShell](https://github.com/PowerShell/PowerShell) using [Scoop](scoop.md):

```shell
scoop install main/pwsh
```

### Update PowerShell

PowerShell cannot be updated while in use. Use `Windows PowerShell` to update `PowerShell`:

* Launch `powershell.exe`

```shell
scoop update main/pwsh
scoop cleanup --cache main/pwsh
```

## Unrestricted PowerShell

If `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` fails, you should use [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy) to run [Scoop](https://scoop.sh).

### Install Unrestricted PowerShell

* download [Unrestricted PowerShell latest release](https://github.com/nicerloop/pwsh-noexecpolicy/releases/latest)
* unzip `PowerShell-NoExecPolicy-XXX-win-x64.zip`
* open `PowerShell-NoExecPolicy-XXX-win-x64` folder
* run `pwsh.exe`
* install [Scoop](https://scoop.sh):

```powershell
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

* install [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy) using [Scoop](https://scoop.sh)

```shell
scoop bucket add nicerloop https://github.com/nicerloop/scoop-nicerloop
scoop config no_junction true
scoop install nicerloop/pwsh
scoop hold pwsh
scoop config no_junction false
exit
```

* delete `PowerShell-NoExecPolicy-XXX-win-x64` folder
* delete `PowerShell-NoExecPolicy-XXX-win-x64.zip`

### Use Unrestricted PowerShell

Ensure you use `pwsh` instead of `powershell` when you use a command line:

* ![PowerShell black icon](https://raw.githubusercontent.com/PowerShell/PowerShell/master/assets/Powershell_black_64.png "PowerShell black icon") `pwsh` is PowerShell (versions 7 and later, previously known as PowerShell Core for version 6)
* ![PowerShell blue icon](https://raw.githubusercontent.com/PowerShell/PowerShell/master/assets/Powershell_64.png "PowerShell blue icon") `powershell` is Windows PowerShell (versions up to 5.1)

You can set `PowerShell` as the defautl profile in [Windows Terminal](windows-terminal.sh).

### Check for updated Unrestricted PowerShell

[PowerShell](https://github.com/PowerShell/PowerShell) checks for new releases and signal when they are available.

To check a new release of [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy) has been made available following the release of official [PowerShell](https://github.com/PowerShell/PowerShell), ask [Scoop](https://scoop.sh):

```shell
scoop status
```

### Update Unrestricted PowerShell

Install new [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy) version:

```shell
scoop config no_junction true
scoop config ignore_running_processes true
scoop unhold pwsh
scoop update nicerloop/pwsh
scoop hold pwsh
scoop config no_junction false
scoop config ignore_running_processes false
exit
```

Close all runing instances of the old version of [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy).

Open a new [Unrestricted PowerShell](https://github.com/nicerloop/pwsh-noexecpolicy) terminal and remove the old version:

```shell
scoop cleanup --cache nicerloop/pwsh
```
