FROM wlniao/dotnet:deps7
ENV DOTNET_FILE=/usr/local/bin
RUN curl -o /tmp/dotnet-sdk.tar.gz https://download.visualstudio.microsoft.com/download/pr/32e09cf3-b5ad-453e-aaa0-2b5c7422141f/6c7f4e895d6aa29471e05367d9880b6c/dotnet-sdk-6.0.404-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet-sdk.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin \
    && echo /dev/null > /tmp/dotnet-sdk.tar.gz
ADD dotnet-sdk-6.0.303-linux-musl-x64.tar.gz /usr/local/bin
RUN export PATH=$PATH:$DOTNET_ROOT:$DOTNET_ROOT/tools

