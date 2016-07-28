FROM ubuntu:trusty
MAINTAINER WlniaoStudio <ideploy@wlniao.com>
ENV WLN_STARTUP_ROOT /wln
ENV WLN_LISTEN_PORT 5000
EXPOSE 5000

RUN	apt-get update \
	&& apt-get install -y curl \
		libicu52 liblldb-3.6 liblttng-ust0 libunwind8 \
		clang-3.5 \
	&& apt-get -y autoremove \
	&& apt-get -y clean \
	&& rm -rf /var/lib/apt/lists/*

# Install .NET Core
ENV DOTNET_VERSION 1.0.0
ENV DOTNET_DOWNLOAD_URL https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/$DOTNET_VERSION/dotnet-ubuntu-x64.$DOTNET_VERSION.tar.gz

RUN curl -SL $DOTNET_DOWNLOAD_URL --output dotnet.tar.gz \
    && mkdir -p /usr/share/dotnet \
    && tar -zxf dotnet.tar.gz -C /usr/share/dotnet \
    && rm dotnet.tar.gz \
    && ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet


WORKDIR /wln
ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN dotnet restore