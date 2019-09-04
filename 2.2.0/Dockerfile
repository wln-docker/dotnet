FROM microsoft/dotnet:2.2-aspnetcore-runtime
MAINTAINER WlniaoStudio <wlniao@qq.com>

ADD ngrok /usr/bin/ngrok
RUN apt-get update && apt-get install -y libgdiplus \
&& ln -s /usr/lib/libgdiplus.so /usr/lib/gdiplus.dll \
&& ln -s /lib/x86_64-linux-gnu/libdl-2.24.so /lib/x86_64-linux-gnu/libdl.so \
&& apt-get clean && rm -rf /var/lib/apt/lists/* && rm -rf /tmp/* \
&& chmod 777 /usr/bin/ngrok

ONBUILD COPY . /wln
ONBUILD WORKDIR /wln