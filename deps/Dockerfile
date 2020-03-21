FROM alpine:3.11
LABEL Maintainer="Wlniao <wlniao@qq.com>" \
      Description="Dotnet container based on Alpine Linux."

RUN apk --no-cache add ca-certificates \
	krb5-libs \
	libgdiplus \
	libstdc++ \
	libssl1.1 \
	libintl \
	libgcc \
	openssl \
	curl \
	zlib \
	icu \
	--repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ && rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/*