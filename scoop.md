# Scoop

To install numerous tools for Windows, usually without requiring elevated rights, you can use [Scoop](https://scoop.sh).

## Standard install

In a PowerShell command window:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

### Restricted PowerShell

If `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` fails, see [Unrestricted PowerShell](powershell.md#unrestricted-powershell) install procedure.

### HTTP proxy install

If access to the Internet is through a HTTP proxy:

* [install Scoop behind a proxy](https://github.com/ScoopInstaller/Scoop/wiki/Using-Scoop-behind-a-proxy#installation):

```powershell
[Net.WebRequest]::DefaultWebProxy = New-Object Net.WebProxy "http://<host>:<port>"
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

* [configure Scoop to use the proxy](https://github.com/ScoopInstaller/Scoop/wiki/Using-Scoop-behind-a-proxy#configuring-scoop-to-use-your-proxy):

```shell
scoop config proxy <host>:<port>
```

### HTTP proxy PAC install

If access to the Internet is through a HTTP proxy configured with PAC:

* [setup a temporary Px](px#temporary-pac-setup) local HTTP proxy handling PAC
* [install Scoop behind a proxy](#http-proxy-install) located at `localhost:3128`
* [install Px](px#standard-install) using [Scoop](https://scoop.sh)
* [remove the temporary Px](px#teardown-temporary-setup)
* [configure PAC and start Px](px#configure-pac-and-start)

## Package discovery

Many packages are available through [Scoop](https://scoop.sh).
You can browse and search the package registry from the main page.

## Package update

[Update](https://github.com/ScoopInstaller/Scoop/wiki/Commands) installed packages, then [remove](https://github.com/ScoopInstaller/Scoop/wiki/Commands) obsolete versions:

```shell
scoop update --all
scoop cleanup --cache --all
```

### PowerShell update

PowerShell cannot be updated while in use; see [Update Powershell](powershell.md#update-powershell) or [Update Unrestricted PowerShell](powershell.md#update-unrestricted-powershell) depending on the version you installed.
