FROM microsoft/dotnet:1.0.0-preview2-nanoserver-sdk
MAINTAINER WlniaoStudio <ideploy@wlniao.com>
ENV WLN_STARTUP_ROOT /wln
ENV WLN_LISTEN_PORT 5000
EXPOSE 5000
WORKDIR /wln
ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN dotnet restore