FROM debian:jessie
MAINTAINER WlniaoStudio <wlniao@qq.com>

RUN apt-get update && apt-get install -y ca-certificates \
	libc6 \
	libcurl3 \
	libgcc1 \
	libgssapi-krb5-2 \
	libicu52 \
	liblttng-ust0 \
	libssl1.0.0 \
	libstdc++6 \
	libunwind8 \
	libuuid1 \
	zlib1g \
	curl \
    && rm -rf /var/lib/apt/lists/*
	
ONBUILD EXPOSE 5000
ONBUILD ENV WLN_STARTUP_ROOT /wln
ONBUILD WORKDIR /wln
