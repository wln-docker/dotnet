FROM windowsservercore
MAINTAINER WlniaoStudio <ideploy@wlniao.com>
ENV WLN_STARTUP_ROOT /wln
ENV WLN_LISTEN_PORT 5000
EXPOSE 5000

# Install .NET Core SDK
ENV DOTNET_SDK_VERSION 1.0.0-preview2-003121
ENV DOTNET_SDK_DOWNLOAD_URL https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/$DOTNET_SDK_VERSION/dotnet-dev-win-x64.$DOTNET_SDK_VERSION.zip

RUN powershell -NoProfile -Command \
        $ErrorActionPreference = 'Stop'; \
        Invoke-WebRequest %DOTNET_SDK_DOWNLOAD_URL% -OutFile dotnet.zip; \
        Expand-Archive dotnet.zip -DestinationPath '%ProgramFiles%\dotnet'; \
        Remove-Item -Force dotnet.zip

RUN setx /M PATH "%PATH%;%ProgramFiles%\dotnet"

# Trigger the population of the local package cache  
ENV NUGET_XMLDOC_MODE skip  
RUN mkdir warmup \  
    && cd warmup \  
    && dotnet new \  
    && cd .. \  
    && rmdir /q/s warmup
WORKDIR /wln
ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN dotnet restore