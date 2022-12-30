FROM wlniao/dotnet:deps6
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/44b5aaf3-48fd-4aac-94bd-5a63318bcc2e/5c2b11a17492763a89dfd061090f7cf5/dotnet-runtime-6.0.9-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/e70c3a5e-bf8e-4995-a84e-1ebb68844980/586fce2fa823fe1d7b44948bc35255e9/aspnetcore-runtime-6.0.9-linux-musl-x64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln