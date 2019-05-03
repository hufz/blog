---
title: 配置jdk，maven
date: 2019-04-11 14:32:17
---
#### jdk
1. 下载jdk:   
wget -P /mnt/download/jdk  http://download.oracle.com/otn-pub/java/jdk/8u161-b12/2f38c3b165be4555a1fa6e98c45e0808/jdk-8u161-linux-x64.tar.gz
2. 下载文件并重命名:   
wget -c http://download.oracle.com/otn-pub/java/jdk/8u181-b13/96a7b8442fe848ef90c96a2fad6ed6d1/jdk-8u181-linux-x64.tar.gz?AuthParam=1535356009_8e01bd0f3fe29cadba788f49f0832967 -O jdk-8u181-linux-x64.tar.gz
3. 将jdk安装包解压到指定目录/mnt/soft/:   
tar -zxvf jdk-8u181-linux-x64.tar.gz -C /mnt/soft/
4. 配置jdk环境变量:   
vim /etc/profile   
export JAVA_HOME=/mnt/soft/jdk1.8.0_181
export PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
5. 配置生效:source /etc/profile
6. 验证jdk是否配好:java -version

#### maven
1. 下载maven  
wget -P /mnt/download/maven/ -c http://mirrors.shu.edu.cn/apache/maven/maven-3/3.5.4/binaries/apache-maven-3.5.4-bin.tar.gz -O apache-maven-3.5.4-bin.tar.gz
2. 解压maven到指定目录  
tar -zxvf /mnt/download/maven/apache-maven-3.5.4-bin.tar.gz -C /mnt/soft/
3. 配置maven  
vim /etc/profile
export MAVEN_HOME=/mnt/soft/apache-maven-3.5.4
export PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$PATH
4. 配置生效   
source /etc/profile
5. 验证maven是否配好  
mvn -version



