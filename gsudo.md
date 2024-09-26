# gsudo

[gsudo](https://gerardog.github.io/gsudo) runs commands with elevated permissions.

## Standard install

If you have elevated username/password credentials, you can install [gsudo](https://gerardog.github.io/gsudo) with [Scoop](scoop.md):

```shell
scoop install main/gsudo
```

## Ivanti Self-elevate

If you have Ivanti Application Control self-elevation, you should install [ivanti-gsudo](https://github.com/nicerloop/ivanti-self-elevate) with [Scoop](scoop.md):

```shell
scoop bucket add nicerloop https://github.com/nicerloop/scoop-nicerloop
scoop install nicerloop/ivanti-gsudo
```
