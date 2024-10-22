# Visual Studio

[Visual Studio](https://visualstudio.microsoft.com/) is an IDE for Microsoft Windows.
It also provides a toolchain to build applications for Microsoft Windows.
Different [editions](https://visualstudio.microsoft.com/vs/compare/) are available.

[Build Tools for Visual Studio](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2022) allow you to build Visual Studio projects from a command-line interface. Use of this tool requires a valid Visual Studio license, unless you are building open-source dependencies for your project.

## Standard install

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[Visual Studio](https://visualstudio.microsoft.com/) editions can be installed using [WinGet](winget.md) and [gsudo](gsudo.md):

```shell
gsudo winget install Microsoft.VisualStudio.2022.Community
```

```shell
gsudo winget install Microsoft.VisualStudio.2022.Professional
```

```shell
gsudo winget install Microsoft.VisualStudio.2022.Enterprise
```

## Build Tools for Visual Studio 2022

:warning: :name_badge: This requires elevated privileges :name_badge: :warning:

[Build Tools for Visual Studio 2022](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2022) can be installed using [WinGet](winget.md) and [gsudo](gsudo.md):

```shell
gsudo winget install Microsoft.VisualStudio.2022.BuildTools
```

