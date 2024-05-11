# wlniao/dotnet:8.0.0

### Build
```
docker build -t wlniao/dotnet:latest -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.0 -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.0-alpine -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.0-debian -f Dockerfile-debian . && \
docker build -t wlniao/dotnet:8.0.0-ubuntu -f Dockerfile-ubuntu . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:latest -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0 -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-alpine -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-debian -f Dockerfile-debian . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-ubuntu -f Dockerfile-ubuntu . && \
docker push wlniao/dotnet:latest && \
docker push wlniao/dotnet:8.0.0 && \
docker push wlniao/dotnet:8.0.0-alpine && \
docker push wlniao/dotnet:8.0.0-debian && \
docker push wlniao/dotnet:8.0.0-ubuntu && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:latest && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0 && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-alpine && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-debian && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.0-ubuntu && \
docker save -o /mnt/8.0.0-ubuntu.tar wlniao/dotnet:8.0.0-ubuntu && \
docker save -o /mnt/8.0.0-debian.tar wlniao/dotnet:8.0.0-debian && \
docker save -o /mnt/8.0.0-alpine.tar wlniao/dotnet:8.0.0-alpine && \
docker images
```