# 基础镜像

> 安装基本的软件包，开启ssh，允许root登陆，默认密码：123456

```shell
docker build -t base:v1 .

docker run --name test -p 20001:22 -d base:v1
```