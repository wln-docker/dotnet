FROM amd64/ubuntu:focal
LABEL Maintainer="Wlniao <wlniao@qq.com>"
RUN apt-get update && apt-get install -y --no-install-recommends ca-certificates \
	libgdiplus \
	libgcc1 \
	libgssapi-krb5-2 \
	libicu66 \
	libssl1.1 \
	openssl \
	curl \
	&& rm -rf /var/lib/apt/lists/*
RUN dotnet_version=3.1.22 \
    && curl -fSL --output dotnet.tar.gz https://dotnetcli.azureedge.net/dotnet/Runtime/$dotnet_version/dotnet-runtime-$dotnet_version-linux-x64.tar.gz \
    && dotnet_sha512='4e32b45086fbd630622d20b0b2316d0c9bd66647b38ef1475c9bf8ef755bd60ec7eb8055a8de2bf89ed96e0460abc9e68f500189dd5437e21f2dfbd4fc71693e' \
    && echo "$dotnet_sha512  dotnet.tar.gz" | sha512sum -c - \
    && curl -fSL --output aspnetcore.tar.gz https://dotnetcli.azureedge.net/dotnet/aspnetcore/Runtime/$dotnet_version/aspnetcore-runtime-$dotnet_version-linux-x64.tar.gz \
    && aspnetcore_sha512='32332a09a2f05e56ca66fff2a27e988dc35dc12dcc312b62c99c2a7b2532fb02bab0fa7f49f73938999488c0463a0c79c151b020e01104b8e9cfab80a877b5f3' \
    && echo "$aspnetcore_sha512  aspnetcore.tar.gz" | sha512sum -c - \
    && mkdir -p /usr/share/dotnet \
    && tar -ozxf dotnet.tar.gz -C /usr/share/dotnet \
    && tar -ozxf aspnetcore.tar.gz -C /usr/share/dotnet ./shared/Microsoft.AspNetCore.App \
    && ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet \
    && ln -s /usr/lib/libgdiplus.so /usr/lib/gdiplus.dll \
    && echo /dev/null > dotnet.tar.gz && rm dotnet.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln

