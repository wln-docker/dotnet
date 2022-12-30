FROM wlniao/dotnet:deps7
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/bbbb66d6-7325-4758-bf39-c6b87a248a1f/4134186ccfb37cc2556211bf76ce1385/dotnet-runtime-6.0.12-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/40ff372d-40dc-4023-a67f-7fa4e9727e74/8d7c35f2115e07a0716bab279fd992be/aspnetcore-runtime-6.0.12-linux-musl-x64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln
ONBUILD RUN mkdir -p /wln/fonts && rm -rf /usr/share/fonts && ln -s /wln/fonts /usr/share/fonts && fc-cache