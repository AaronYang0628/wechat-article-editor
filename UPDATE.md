# Docker 镜像

## 构建镜像并发布

### 0. Docker 账号登录

执行以下命令，登录 Docker 账号：

```bash
docker login -u <username> -p <password>
```

### 1. 构建镜像

分别执行以下四个命令：

```bash
bash scripts/build-base-image.sh
```

```bash
bash scripts/build-nginx.sh
```

```bash
bash scripts/build-standalone.sh
```

```bash
bash scripts/build-static.sh
```

### 2. 推送镜像

构建出工具镜像后，执行以下命令：

```bash
bash scripts/push-images.sh
```

将镜像推送至 Docker Hub。

## 拉取、运行镜像

执行以下命令进行镜像拉取：

```bash
docker pull doocs/md:latest
```

运行镜像：

```bash
# docker run -d -p 8888:80 doocs/md:latest
docker run -d -p 8888:80 crpi-wixjy6gci86ms14e.cn-hongkong.personal.cr.aliyuncs.com/ay-dev/wechat-article-editor:v20251113r0
```
