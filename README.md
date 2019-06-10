# docker-php

基于 Docker 的 php 运行环境

compose 文件将运行三个容器：php、postgres、nginx

或是直接进入容器中，在 命令行 下执行 php 代码

## 使用说明

### ./app 目录

该目录会被映射至 nginx 及 php 容器中的 /app 目录下

我们可以将项目代码放在此目录中，与容器进行共享:

```
./app/foo  // 项目代码 foo
./app/bar  // 项目代码 bar
```

### ./nginx 目录

在 ./nginx/services 中配置项目的服务文件

注意完成配置后，需要将对应的端口暴露出来，使主机能够进行访问


在 docker-compose.yml 文件中，将应用的服务端口暴露至主机

运行下面的代码，启动运行环境

``` bash
# run
docker-compose up -d --build

# stop
docker-compose down
```
