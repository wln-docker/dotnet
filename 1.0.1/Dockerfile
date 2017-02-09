FROM ubuntu:trusty
MAINTAINER WlniaoStudio <ideploy@wlniao.com>
ENV WLN_STARTUP_ROOT /wln
ENV WLN_LISTEN_PORT 5000
EXPOSE 5000

RUN LIBUV_VERSION=1.9.1 \
	&& apt-get update \
	&& apt-get -y install git vim curl autoconf automake build-essential libtool \
	&& curl -sSL https://github.com/libuv/libuv/archive/v${LIBUV_VERSION}.tar.gz | tar zxfv - -C /usr/local/src \
	&& cd /usr/local/src/libuv-$LIBUV_VERSION \
	&& sh autogen.sh && ./configure && make && make install \
	&& rm -rf /usr/local/src/libuv-$LIBUV_VERSION \
	&& ldconfig 

RUN apt-get install -y apt-transport-https libicu52 liblldb-3.6 liblttng-ust0 libunwind8 clang-3.5 \
    && echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet/ trusty main" > /etc/apt/sources.list.d/dotnetdev.list \
    && apt-key adv --keyserver apt-mo.trafficmanager.net --recv-keys 417A0893 \
    && apt-get update
RUN apt-get install -y dotnet-dev-1.0.0-preview2-003131
	
WORKDIR /wln
ENTRYPOINT ["dotnet", "run"]
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN dotnet restore