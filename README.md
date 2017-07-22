linux安装jdk    
CentOS下jdk的安装（安装hadoop教程装的是tar包格式的）        
mkdir /export/software 创建安装包的目录        
Jdk的安装包拷贝在了目录/export/software下    
mkdir /export/servers 创建安装目录    
tar -zxvf jdk-8u73-linux-x64.tar.gz -C /export/servers/    
cd /export/servers/    
ll    
ln –s jdk1.8.0_73 jdk 创建软链接    
cd jdk    
ll    
pwd    
vi /etc/profile 配置环境变量    

在最后边添加    
#set java env    
export JAVA_HOME=/export/servers/jdk    
export JRE_HOME=${JAVA_HOME}/jre    
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib    
export PATH=${JAVA_HOME}/bin:$PATH    

source /etc/profile 使配置文件生效    
java –version 看是否安装好    
完成    
    
