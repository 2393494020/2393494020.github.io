#### 常用运维命令

docker pull alpine  
docker pull `<image name>`  
docker run --name `<container name>` `[-i][-t][-d][-p <host_port:container_port>]` `<image:tag>` `<shell>`  
docker images  
docker ps -a  
docker kill `<container id>`  
docker rm `<container id>`  
docker rm `$(docker ps -a -q)`  
docker rmi `<image id>`  
docker start `<container id>`  
docker attach `<container id>`  
docker exec -it `<container id>` `<shell>`  
docker build -t `<my image name>` .  
docker commit -m 'message...' `<container id>` `<image name>`:`<tag>`   

#### 加速

```
# vi /etc/docker/daemon.json
{
    "registry-mirrors": ["https://docker.mirrors.ustc.edu.cn"]
}
```

#### 参考资源

https://blog.csdn.net/kcp606/article/details/79167898  
https://www.cnblogs.com/river2005/p/8283700.html  
https://linux.cn/article-9541-1-rel.html  
https://blog.csdn.net/qq_40794266/article/details/83793241  
https://blog.csdn.net/qq_33285112/article/details/78593906

#### Dockerfile

``` Dockerfile
FROM ubuntu
RUN apt-get update && apt-get install -y vim zip unzip net-tools iputils-ping openssh-client openssh-server
# for c++
# RUN apt-get install -y g++ autoconf automake libtool cmake zlib1g-dev pkg-config libssl-dev

RUN ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
RUN cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
RUN chmod 0600 ~/.ssh/authorized_keys

RUN mkdir /opt/java
ADD /opt/java/jdk-8u162-linux-x64.tar.gz /opt/java
ADD /home/dist/hadoop-3.2.0.tar.gz /opt/java
RUN cd /opt/java && tar -xzvf jdk-8u162-linux-x64.tar.gz && mv jdk1.8.0_162 jdk
RUN cd /opt/java && tar -xzvf hadoop-3.2.0.tar.gz && mv hadoop-3.2.0 hadoop
RUN sed -i '$a\export JAVA_HOME=/opt/java/jdk' /etc/profile
RUN sed -i '$a\export HADOOP_HOME=/opt/java/hadoop' /etc/profile
RUN sed -i '$a\export PATH=.:$PATH:$JAVA_HOME/bin:$HADOOP_HOME/bin' /etc/profile
```