FROM wlniao/dotnet:deps
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/a5ff9cbb-d558-49d1-9fd2-410cb1c8b095/a940644f4133b81446cb3733a620983a/dotnet-runtime-3.0.0-linux-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/2dd89dc5-add5-4582-9a72-7c55f447a069/ef2d3aa1e91e837a8400d5e69fc6952f/aspnetcore-runtime-3.0.0-linux-musl-x64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln

