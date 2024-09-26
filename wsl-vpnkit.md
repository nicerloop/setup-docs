# wsl-vpnkit

[wsl-vpnkit](https://github.com/sakai135/wsl-vpnkit) provides network connectivity to [WSL 2](wsl.md) when blocked by VPN.

## Standard install

[wsl-vpnkit](https://github.com/sakai135/wsl-vpnkit) can be installed with [Scoop](scoop.sh):

```shell
scoop bucket add srsrns https://github.com/mbl-35/scoop-srsrns
scoop install srsrns/wsl-vpnkit
```

## Setup wsl-vpnkit to start on login

Create a startup shortcut (this shortcut uses the icon provided by [wsl-vpnkit-tray](wsl-vpnkit-tray.md)):

```powershell
$Shortcut=(New-Object -COM WScript.Shell).CreateShortcut("$env:USERPROFILE\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\Wsl Vpnkit.lnk")
$Shortcut.TargetPath="C:\Windows\system32\wsl.exe"
$Shortcut.Arguments="--distribution wsl-vpnkit service wsl-vpnkit start"
$Shortcut.WindowStyle=7
$Shortcut.IconLocation="$env:USERPROFILE\scoop\apps\wsl-vpnkit-tray\current\wsl-vpnkit-tray.ico"
$Shortcut.Save()
```
