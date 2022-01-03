FROM wlniao/dotnet:deps
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/787e6ae7-03a1-44c3-849f-ed85b25ff620/c6f4cfe60b5dc12cb2032a580c8e4c58/dotnet-runtime-3.1.22-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/a5bdf73f-4a49-41d4-a401-faf92dda842c/c8b17243ecf466c9124bb5fa46d10354/aspnetcore-runtime-3.1.22-linux-musl-arm64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln

