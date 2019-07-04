#初始镜像
FROM centos:centos7

#维护者信息
MAINTAINER yongxuezhen

#下载jdk，解压，创建软连接
RUN mkdir /soft && cd /soft && yum -y install wget && wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u141-b15/336fa29ff2bb4ef291e347e091f7f4a7/jdk-8u141-linux-x64.tar.gz" && tar -zxvf jdk-8u141-linux-x64.tar.gz  && ln -s jdk1.8.0_141/ jdk

#配置环境变量
ENV JAVA_HOME /soft/jdk
ENV PATH $JAVA_HOME/bin:$PATH

#启动时执行的命令
CMD ["/bin/bash"]