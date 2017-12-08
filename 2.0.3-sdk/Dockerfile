FROM wlniao/dotnet:deps2.0
MAINTAINER WlniaoStudio <wlniao@qq.com>

RUN apt-get update && apt-get install -y git vim && rm -rf /var/lib/apt/lists/*
RUN curl -SL https://get.wlniao.com/dotnet/download-sdk/dotnet-sdk-2.0.3-linux-x64.tar.gz --output dotnet.tar.gz \
    && mkdir -p /usr/share/dotnet \
    && tar -zxf dotnet.tar.gz -C /usr/share/dotnet \
    && rm dotnet.tar.gz \
    && rm -rf /var/lib/apt/lists/* \
    && ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet

ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN dotnet restore