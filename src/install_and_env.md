

# 基础环境准备


## （一）下载
**开发环境，一般还是推荐直接从oracle下载**
```
https://www.oracle.com/java/technologies/downloads/#java8
https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html
https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html
https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html
```
**生产环境，一般推荐直接使用docker镜像**
```
```

## （二）安装
### MacOS
下载的是dmg就直接双击安装，下载的是压缩包就解压到相应目录。  
推荐dmg，简单一些。
可以同时安装多个版本，在MacOS的安装目录是在
```
/Library/Java/JavaVirtualMachines/jdk-11.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home

```
可以通过下列命令查看具体安装，
```
/usr/libexec/java_home -V
```

### windows

### linux

## （三）灵活切换版本
**可以使用如下脚本进行：**
``` ~/.bash_profile
JAVA_HOME_21=/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home
JAVA_HOME_17=/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
JAVA_HOME_8=/Library/Java/JavaVirtualMachines/jdk1.8.0_291.jdk/Contents/Home

JRE_HOME=$JAVA_HOME/jre
PATH=$PATH:$JAVA_HOME/bin
CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.

export JRE_HOME
export PATH
export CLASSPATH

export JAVA_HOME=$JAVA_HOME_21

alias jdk21="export JAVA_HOME=$JAVA_HOME_21"
alias jdk17="export JAVA_HOME=$JAVA_HOME_17"
alias jdk8="export JAVA_HOME=$JAVA_HOME_8"