FROM ubuntu

RUN apt-get update \
&& apt-get install -y \
ca-certificates \
lsb-release \
tzdata \
net-tools \
iputils-ping \
netcat \
telnet \
vim \
tar zip unzip \
wget curl \
sngrep tcpdump \
openssh-server


RUN if [ ! -d "/run/sshd" ];then mkdir /run/sshd;fi;

# 允许root用户登录
RUN sed -ri 's/^#PermitRootLogin.*$/PermitRootLogin yes/' /etc/ssh/sshd_config;
# 设置容器root用户默认密码
RUN echo 'root:123456' | chpasswd

USER root

# 启动ssh
CMD ["/usr/sbin/sshd", "-D"]