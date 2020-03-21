FROM alpine:3.10
LABEL Maintainer="Wlniao <wlniao@qq.com>" \
      Description="Dotnet container based on Alpine Linux."

RUN apk --no-cache add ca-certificates \
	libgdiplus \
	libstdc++ \
	openssl \
	libintl \
	curl \
	icu \
	--repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ && rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/*