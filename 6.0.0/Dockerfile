FROM wlniao/dotnet:deps6
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/95352809-7f41-40f3-974d-8d530321a8e4/0024d7bf0c872f176ceba7a63a34915b/dotnet-runtime-6.0.0-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/a757153c-6675-4d63-a979-de2f4fede0d4/baa9ed8b963c49d69c725b57352b051d/aspnetcore-runtime-6.0.0-linux-musl-x64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln