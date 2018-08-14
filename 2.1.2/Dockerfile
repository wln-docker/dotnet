FROM wlniao/dotnet:deps2.0
MAINTAINER WlniaoStudio <wlniao@qq.com>

RUN curl -SL https://dotnetcli.blob.core.windows.net/dotnet/Runtime/2.1.2/dotnet-runtime-2.1.2-linux-x64.tar.gz --output dotnet.tar.gz \
    && mkdir -p /usr/share/dotnet \
    && tar -zxf dotnet.tar.gz -C /usr/share/dotnet \
    && rm dotnet.tar.gz \
    && ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet

ONBUILD COPY . /wln
ONBUILD WORKDIR /wln