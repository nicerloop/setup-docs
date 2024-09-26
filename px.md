# Px

[Px](https://github.com/genotrance/px) is a HTTP proxy server to automatically authenticate to an upstream HTTP proxy, or to handle proxy autoconfiguration (PAC). 

## Standard install

```shell
scoop install main/px
```

## Configure PAC and start

[Configure Px](https://github.com/genotrance/px#misc) upstream Proxy Auto-Configuration:

```shell
px --config=$HOME\px.ini --save --pac=<upstream.pac.url> --hostonly
```

[Setup Px](https://github.com/genotrance/px/issues/213#issuecomment-2019863160) to start in background on login without window:

```powershell
Set-ItemProperty -Path HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run -Name Px -Value "$HOME\scoop\apps\px\current\pythonw.exe -m px --config=$HOME\px.ini"
```

[Start Px](https://github.com/genotrance/px#misc) from the command line:

```powershell
& "$HOME\scoop\apps\px\current\pythonw" -m px --config=$HOME\px.ini
```

You should now use `http://localhost:3128`(Windows) or `http://$(hostname).local:3128`(WSL) as proxy configuration in your tools.

## Temporary PAC setup

* Download [Px 0.9.2 for Windows](https://github.com/genotrance/px/releases/download/v0.9.2/px-v0.9.2-windows-amd64.zip)
* Extract archive to `px-v0.9.2-windows-amd64` folder
* Open a Powershell window inside Px folder
* Run Px

```shell
./px --foreground --pac=<PAC_URL>
```

You now have a local forwarding HTTP proxy connected to the the upstream HTTP proxy through PAC.

### Teardown temporary setup

* stop the currently running `Px` application using `[CTRL-C]`
* delete the `px-v0.9.2-windows-amd64` temporary forwarder
