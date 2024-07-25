# wlniao/dotnet:8.0.4

### Build
```
docker build -t wlniao/dotnet:8.0.4-alpine -f Dockerfile-alpine . && \
docker build -t wlniao/dotnet:8.0.4-debian -f Dockerfile-debian . && \
docker build -t wlniao/dotnet:8.0.4-ubuntu -f Dockerfile-ubuntu . && \
docker build -t wlniao/dotnet:8.0.4-gdi -f Dockerfile-gdi . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-alpine -f Dockerfile-alpine . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-debian -f Dockerfile-debian . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-ubuntu -f Dockerfile-ubuntu . && \
docker build -t ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-gdi -f Dockerfile-gdi . && \
docker push wlniao/dotnet:8.0.4-alpine && \
docker push wlniao/dotnet:8.0.4-debian && \
docker push wlniao/dotnet:8.0.4-ubuntu && \
docker push wlniao/dotnet:8.0.4-gdi && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-alpine && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-debian && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-ubuntu && \
docker push ccr.ccs.tencentyun.com/wlniao/dotnet:8.0.4-gdi && \
docker save -o /mnt/8.0.4-alpine.tar wlniao/dotnet:8.0.4-alpine && \
docker save -o /mnt/8.0.4-debian.tar wlniao/dotnet:8.0.4-debian && \
docker save -o /mnt/8.0.4-ubuntu.tar wlniao/dotnet:8.0.4-ubuntu && \
docker save -o /mnt/8.0.4-gdi.tar wlniao/dotnet:8.0.4-gdi && \
docker images
```