FROM alpine:3.16
LABEL Maintainer="Wlniao <wlniao@qq.com>" \
      Description="Dotnet container based on Alpine Linux."

RUN apk --no-cache add ca-certificates \
	ttf-opensans \
	krb5-libs \
	libgdiplus \
	libstdc++ \
	libssl1.1 \
	libintl \
	libgcc \
	icu-libs \
	openssl \
	curl \
	zlib \
	icu \
	--repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ && rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/* && \
	ln -s /usr/lib/libgdiplus.so.0.0.0  /usr/lib/libgdiplus.so