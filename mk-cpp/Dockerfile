FROM base:v1

# 设置阿里的ubuntu的源
RUN echo "deb http://mirrors.aliyun.com/ubuntu focal-security main restricted\ndeb http://mirrors.aliyun.com/ubuntu focal-security universe\ndeb http://mirrors.aliyun.com/ubuntu focal-security multiverse\ndeb http://mirrors.aliyun.com/ubuntu focal main restricted\ndeb http://mirrors.aliyun.com/ubuntu focal-updates main restricted\ndeb http://mirrors.aliyun.com/ubuntu focal universe\ndeb http://mirrors.aliyun.com/ubuntu focal-updates universe\ndeb http://mirrors.aliyun.com/ubuntu focal multiverse\ndeb http://mirrors.aliyun.com/ubuntu focal-updates multiverse\ndeb http://mirrors.aliyun.com/ubuntu focal-backports main restricted universe multiverse\n" > /etc/apt/sources.list \
&& echo "-----------------------" \
&& cat /etc/apt/sources.list \
&& echo "-----------------------" \
&& ln -snf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
&& echo Asia/Shanghai >/etc/timezone

# 安装编译工具
RUN apt-get update \
&& apt-get install -y \
build-essential \
gcc \
gdb \
cmake



