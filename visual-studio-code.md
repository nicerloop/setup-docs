# Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) is a cross-platform IDE.

## Standard install

[Visual Studio Code](https://code.visualstudio.com/) can be installed using [Scoop](scoop.md):

```shell
scoop bucket add extras
scoop install extras/vscode
```

## Dev Containers extension with Rancher Desktop

There is a Docker error when starting a container using the [Visual Studio Code Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension with [Rancher Desktop](rancher-desktop.md).

The [workaround](https://docs.rancherdesktop.io/troubleshooting-tips/#q-how-can-i-fix-the-docker-error-when-starting-a-container-using-the-vs-code-dev-containers-extension-with-version-v0266) is to disable Wayland in the user settings: uncheck the box in the Settings > Extensions > Dev Containers tab labelled Dev > Containers: Mount Wayland Socket (Applies to All Profiles).
