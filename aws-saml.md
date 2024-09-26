# AWS with SAML authentication

[saml2aws](https://github.com/Versent/saml2aws) enables you to login and retrieve AWS temporary credentials using a SAML IDP.

## Standard install

[saml2aws](https://github.com/Versent/saml2aws) can be installed using [Scoop](scoop.md):

```shell
scoop install main/saml2aws
```

## Default configuration

Follow [saml2aws documentation](https://github.com/Versent/saml2aws#configuring-idp-accounts) to configure the IdP provider:

```shell
saml2aws configure --skip-prompt --profile default --idp-provider Browser --region "<aws-region>" --url "<aws-saml-sso-url>"
```

On first login, allow downloading Browser drivers:

```shell
saml2aws login --download-browser-driver
```

## Standard usage

Afterwards, you can simply login:

```shell
saml2aws login
```
