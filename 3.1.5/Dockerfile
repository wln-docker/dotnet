FROM wlniao/dotnet:deps
RUN curl -o /tmp/dotnet.tar.gz https://download.visualstudio.microsoft.com/download/pr/56f86fa0-834a-4397-94b4-d4331078c91f/7de4bc57ed6a5cd7dddcefeed7aa1fd6/dotnet-runtime-3.1.5-linux-musl-x64.tar.gz \
    && tar zxf /tmp/dotnet.tar.gz -C /usr/local/bin \
    && curl -o /tmp/aspnetcore.tar.gz https://download.visualstudio.microsoft.com/download/pr/8438f49c-a336-4846-87ae-b3badfb978ee/2b4d72e03ccd0e737657e0534f4e092c/aspnetcore-runtime-3.1.5-linux-musl-x64.tar.gz \
    && tar zxf /tmp/aspnetcore.tar.gz -C /usr/local/bin \
    && chmod 777 /usr/local/bin/dotnet \
    && echo /dev/null > /tmp/dotnet.tar.gz && echo /dev/null > /tmp/aspnetcore.tar.gz
ONBUILD COPY . /wln
ONBUILD WORKDIR /wln

