FROM microsoft/dotnet:2.2-aspnetcore-runtime
MAINTAINER WlniaoStudio <wlniao@qq.com>

RUN apt-get update 
RUN apt-get install -y libgdiplus libfontconfig1 && ln -s /usr/lib/libgdiplus.so /usr/lib/gdiplus.dll
RUN ln -s /lib/x86_64-linux-gnu/libdl-2.24.so /lib/x86_64-linux-gnu/libdl.so
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

ONBUILD /wln
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln