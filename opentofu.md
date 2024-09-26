# OpenTofu

[OpenTofu](https://opentofu.org/) is an open source infrastructure as code tool.
It is a fork of Terraform that is open-source, community-driven, and managed by the Linux Foundation.

## Standard install

Install [OpenTofu](https://opentofu.org/) using [Scoop](scoop.md):

```shell
scoop install main/opentofu
```

## Recommended: Configure OpenTofu as Terraform replacement

Define `TF_CMD` environment variable to use OpenTofu in place of Terraform:

```powershell
[System.Environment]::SetEnvironmentVariable('TF_CMD','tofu', 'User')
```
