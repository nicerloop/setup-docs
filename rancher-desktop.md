# Rancher Desktop

[Rancher Desktop](https://rancherdesktop.io/) is a cross-platform container management environment with a liberal license.

[Rancher Desktop](https://rancherdesktop.io/) provides [Docker](https://www.docker.com/) and [Kubernetes](https://kubernetes.io/) managers.

[Rancher Desktop](https://rancherdesktop.io/) uses [Windows Subsystem for Linux (WSL)](wsl.md) to run containers on Windows.

## Standard install

[Rancher Desktop](https://rancherdesktop.io/) can be installed using [Scoop](scoop.md):

```shell
scoop bucket add extras
scoop install extras/rancher-desktop
```

## Docker default configuration

Start `Rancher Desktop` and configure it:

* Start `Rancher Desktop` from the `Start Menu/Scoop Apps` folder
	* Disable `Kubernetes`
	* Select `dockerd(moby)`
	* Validate and wait until the end of the initialisation procedure
* Open `File/Preferences`
	* Select `Application` section, `Behavior` tab
		* Check `Automatically start at login`
		* Check `Start in the background`
	* `Apply` the configuration
* Close the Rancher Desktop window

Rancher Desktop is still accessible through the system tray

On the command line, test the docker installation:

```shell
docker run --rm hello-world
```

## Optional: Configure HTTP proxy

* Open `Rancher Desktop` from the `Start Menu/Scoop Apps` folder
* Open `File/Preferences`
	* Select `WSL` section, `Proxy` tab
		* Check `Enable the proxy used by rancher-desktop`
		* Configure HTTP proxy host and port
		* Add your domain to the `No proxy hostname list`
	* `Apply` the configuration
* Close the Rancher Desktop window

## Optional: Configure local Px HTTP proxy

Configure the HTTP proxy as described above with the following parameters:

* Get the Windows hostname:

```shell
hostname
```

* Configure the HTTP proxy as described above, with the [Px](px.md) configuration as seen from WSL:
	* host: `<hostname>.local`
	* port: `3128`
