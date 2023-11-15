FROM alpine:3.18
LABEL Maintainer="Wlniao <wlniao@qq.com>" \
      Description="Dotnet container based on alpine."
ENV DOTNET_ROOT /usr/bin/dotnet
ENV PATH $PATH:$DOTNET_ROOT:/wln
RUN apk --no-cache add \
	libgdiplus \
	libstdc++ \
	libssl1.1 \
	libintl \
	krb5-libs \
	icu \
	curl \
	zlib \
	--repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ && rm -rf /var/cache/apk/* && rm -rf /root/.cache && rm -rf /tmp/* && \
	ln -s /usr/lib/libgdiplus.so.0.0.0  /usr/lib/libgdiplus.so

RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/7aa33fc7-07fe-48c2-8e44-a4bfb4928535/3b96ec50970eee414895ef3a5b188bcd/aspnetcore-runtime-8.0.0-linux-musl-x64.tar.gz \
    && mkdir -p $DOTNET_ROOT && tar zxf /tmp/dotnet.tar.gz -C $DOTNET_ROOT \
    && echo /dev/null > /tmp/dotnet.tar.gz \
    && chmod 777 $DOTNET_ROOT  \
    && chmod a+x $DOTNET_ROOT/dotnet \
    && rm -rf /tmp/*