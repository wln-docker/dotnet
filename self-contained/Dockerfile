FROM alpine:3.16
LABEL Maintainer="Wlniao <wlniao@qq.com>" \
      Description="Dotnet container based on Alpine Linux."
ADD https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub /etc/apk/keys/sgerrand.rsa.pub
ADD https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.29-r0/glibc-2.29-r0.apk /tmp/glibc.apk
RUN apk --no-cache add /tmp/glibc.apk ca-certificates openssl krb5-libs libgdiplus libstdc++ libssl1.1 libintl libgcc icu-libs icu zlib \ 
	--repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ && rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/* && \
	ln -s /usr/lib/libgdiplus.so.0.0.0  /usr/lib/libgdiplus.so && \
	rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/*
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln