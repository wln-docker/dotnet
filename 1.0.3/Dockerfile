FROM wlniao/dotnet:deps
MAINTAINER WlniaoStudio <wlniao@qq.com>

RUN curl -SL https://dotnetcli.blob.core.windows.net/dotnet/preview/Binaries/1.0.3/dotnet-debian-x64.1.0.3.tar.gz --output dotnet.tar.gz \
    && mkdir -p /usr/share/dotnet \
    && tar -zxf dotnet.tar.gz -C /usr/share/dotnet \
    && rm dotnet.tar.gz \
    && ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet

ONBUILD COPY . /wln
ONBUILD WORKDIR /wln