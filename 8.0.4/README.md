# wlniao/dotnet:8.0.4

### Build
```
docker build -t wlniao/dotnet:latest -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.4 -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.4-alpine -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.4-debian -f Dockerfile-debian . && \
docker build -t wlniao/dotnet:8.0.4-ubuntu -f Dockerfile-ubuntu . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:latest -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4 -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-alpine -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-debian -f Dockerfile-debian . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-ubuntu -f Dockerfile-ubuntu . && \
docker push wlniao/dotnet:latest && \
docker push wlniao/dotnet:8.0.4 && \
docker push wlniao/dotnet:8.0.4-alpine && \
docker push wlniao/dotnet:8.0.4-debian && \
docker push wlniao/dotnet:8.0.4-ubuntu && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:latest && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4 && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-alpine && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-debian && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-ubuntu && \
docker save -o /mnt/8.0.4-ubuntu.tar wlniao/dotnet:8.0.4-ubuntu && \
docker save -o /mnt/8.0.4-debian.tar wlniao/dotnet:8.0.4-debian && \
docker save -o /mnt/8.0.4-alpine.tar wlniao/dotnet:8.0.4-alpine && \
docker images
```