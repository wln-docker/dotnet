FROM microsoft/dotnet:1.0.0-windowsservercore-core
MAINTAINER WlniaoStudio <ideploy@wlniao.com>

ENV WLN_STARTUP_ROOT /wln
ENV WLN_LISTEN_PORT 5000
EXPOSE 5000
WORKDIR /wln
ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln