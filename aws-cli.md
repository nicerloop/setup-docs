# AWS CLI

[aws-cli](https://aws.amazon.com/cli/) is the command-line interface to interact with AWS services.

## Standard install

Install [aws-cli](https://aws.amazon.com/cli/) using [Scoop](scoop.md):

```shell
scoop install main/aws
```

## Optional: Configure AWS credentials in WSL

Share AWS credentials from Windows to WSL:

```shell
cd $Env:USERPROFILE
wsl
ln -s $(pwd)/.aws $HOME
exit
```
