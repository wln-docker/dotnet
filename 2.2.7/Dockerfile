FROM wlniao/dotnet:deps
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/ae594623-ff74-42a2-8662-8c7364c8d497/b7b01b805df4e665c0e34d5f94ff804c/dotnet-runtime-2.2.7-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo " " > /tmp/dotnet.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln