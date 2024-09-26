# HTTP proxy

Environment variables are conventionally used to define HTTP proxy for command-line tools.

## Declare HTTP proxy for command line tools

Define [`HTTP_PROXY`, `HTTPS_PROXY` environment variables](https://about.gitlab.com/blog/2021/01/27/we-need-to-talk-no-proxy/) environment variables in `User` scope.

```powershell
[System.Environment]::SetEnvironmentVariable('http_proxy','http://<host>:<port>', 'User')
[System.Environment]::SetEnvironmentVariable('https_proxy','http://<host>:<port>', 'User')
```

## Declare HTTP proxy for Java tools

Define [`JAVA_TOOL_OPTIONS`](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/envvars002.html) environment variables in `User` scope with [Java networking properties](https://docs.oracle.com/javase/8/docs/technotes/guides/net/proxies.html).

```powershell
[System.Environment]::SetEnvironmentVariable('JAVA_TOOL_OPTIONS','-Dhttp.proxyHost=<host> -Dhttp.proxyPort=<port> -Dhttps.proxyHost=<host> -Dhttps.proxyPort=<port>', 'User')
```
