# Docker
沙箱代替虚拟机，更小粒度的部署

## 简介
- 文档: https://docs.docker.com/
- 源码: https://github.com/docker/compose
- Docker 容器是将操作系统层虚拟化
- Apache-2.0 license, Go

## 安装

### 可选1：部署 Docker Compose
1. 使用 Dockerfile 定义应用程序环境
2. 使用 docker-compose.yml 定义构成应用程序的服务
3. 运行 docker compose up

### 可选2：安装 Docker Desktop
- https://docs.docker.com/get-docker/
- 支持 Linux，虚拟化支持 macOS、Windows
- 大型企业(超过 250 名员工或年收入超过 1000 万美元)对 Docker Desktop 的商业使用需要付费订阅。
- 提供 GUI

### 可选3：部署 Docker Engine
- https://docs.docker.com/engine/install/
- 仅支持 Linux 包括: Ubuntu、CentOS、Debian、Fedora 等

## 制作镜像

### 定制 `Dockerfile`
- `FROM nginx` 以镜像为基础进行定制（例如运行时、三方库）
```docker
FROM nginx
RUN echo '<h1>Hello, Docker!</h1>' > /usr/share/nginx/html/index.html
```
- `FROM scratch` 不依赖任何镜像（例如静态编译的可执行文件）
```docker
FROM debian:stretch
RUN set -x; buildDeps='gcc libc6-dev make wget' \
    && apt-get update \
    && apt-get install -y $buildDeps \
    && wget -O redis.tar.gz "http://download.redis.io/releases/redis-5.0.3.tar.gz" \
    && mkdir -p /usr/src/redis \
    && tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 \
    && make -C /usr/src/redis \
    && make -C /usr/src/redis install \
    && rm -rf /var/lib/apt/lists/* \
    && rm redis.tar.gz \
    && rm -r /usr/src/redis \
    && apt-get purge -y --auto-remove $buildDeps
```
### 构建 `Dockerfile`
- 使用 `docker build` 命令进行镜像构建
```docker
$ docker build -t nginx:v3 .
Sending build context to Docker daemon 2.048 kB
Step 1 : FROM nginx
 ---> e43d811ce2f4
Step 2 : RUN echo '<h1>Hello, Docker!</h1>' > /usr/share/nginx/html/index.html
 ---> Running in 9cdc27646c7b
 ---> 44aa4490ce2c
Removing intermediate container 9cdc27646c7b
Successfully built 44aa4490ce2c
```
- 支持从 URL 构建，比如 Git repo
```docker
# $env:DOCKER_BUILDKIT=0
# export DOCKER_BUILDKIT=0

$ docker build -t hello-world https://github.com/docker-library/hello-world.git#master:amd64/hello-world

Step 1/3 : FROM scratch
 --->
Step 2/3 : COPY hello /
 ---> ac779757d46e
Step 3/3 : CMD ["/hello"]
 ---> Running in d2a513a760ed
Removing intermediate container d2a513a760ed
 ---> 038ad4142d2b
Successfully built 038ad4142d2b
```

