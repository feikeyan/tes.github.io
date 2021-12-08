# 测试案例

nohup java -jar hospital.jar >log.txt &



# 阿里云服务器

外网面板地址: http://47.104.79.18:8888/3935c608
内网面板地址: http://172.21.27.85:8888/3935c608
username: kvjxfd9c
password: e3528710





外网面板地址: http://123.60.24.7:8888/7f96954f
内网面板地址: http://192.168.0.204:8888/7f96954f
username: 8ivoz4oa
password: a182d783



# 华为云

外网面板地址: http://123.60.24.7:8888/7f96954f
内网面板地址: http://192.168.0.204:8888/7f96954f
username: 8ivoz4oa
password: 8a16eb6a





4ae83e4b

yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh



文件改名字

mv jdk1.8.0_191/ jdk



47.104.79.18  公有ip

172.21.27.85 私有ip

vi /etc/profile



JAVA_HOME=/root/java/jdk 
JRE_HOME=/root/java/jdk/jre 
PATH=$PATH:$JAVA_HOME/bin:$JRE_HOME/bin CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib
export JAVA_HOME JRE_HOME PATH CLASSPATH



source /etc/profile





# mysql密码

1.下载

```
wget http://dev.mysql.com/get/mysql57-community-release-el7-10.noarch.rpm
yum -y install mysql57-community-release-el7-10.noarch.rpm
yum -y install mysql-community-server
```

![img](https://img.alicdn.com/tfs/TB1ka91h_M11u4jSZPxXXahcXXa-958-431.png)

2. 执行以下命令，启动 MySQL 数据库。

```
systemctl start mysqld.service
```

3. 执行以下命令，查看MySQL初始密码。

```
grep "password" /var/log/mysqld.log
```

![img](https://img.alicdn.com/tfs/TB1HCX6RQY2gK0jSZFgXXc5OFXa-834-36.png)

4. 执行以下命令，登录数据库。

```
mysql -uroot -p
```

5. 执行以下命令，修改MySQL默认密码。

```
set global validate_password_policy=0;  #修改密码安全策略为低（只校验密码长度，至少8位）。
ALTER USER 'root'@'localhost' IDENTIFIED BY '12345678';
```

6. 执行以下命令，授予root用户远程管理权限。

```
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '12345678';
```

7. 修改密码为12345678
8. 输入exit退出数据库。

D:\Download\Utilities\macrecovery



https://yb12hx1m.mirror.aliyuncs.com



# Tomcat端口

###  安装Tomcat

###  1. 执行以下命令，下载Tomcat压缩包。

```
wget https://mirrors.tuna.tsinghua.edu.cn/apache/tomcat/tomcat-8/v8.5.69/bin/apache-tomcat-8.5.69.tar.gz
```

2. 执行以下命令，解压刚刚下载Tomcat包。

```
tar -zxvf apache-tomcat-8.5.69.tar.gz 
```

3. 执行以下命令，修改Tomcat名字。

```
mv apache-tomcat-8.5.69 /usr/local/Tomcat8.5
```

4. 执行以下命令，为Tomcat授权。

```
chmod +x /usr/local/Tomcat8.5/bin/*.sh
```

5. 执行以下命令，修改Tomcat默认端口号为80。

说明： Tomcat默认端口号为8080。

```
sed -i 's/Connector port="8080"/Connector port="80"/' /usr/local/Tomcat8.5/conf/server.xml
```

![img](https://img.alicdn.com/tfs/TB1WX9jilBh1e4jSZFhXXcC9VXa-829-794.png)

6. 启动Tomcat。

```
/usr/local/Tomcat8.5/bin/./startup.sh
```

7. 访问Tomcat。

打开浏览器，在地址栏中输入ECS公网IP，例如：139.0.0.1

如果显示如下界面，则表示Tomcat安装配置成功。

![img](https://img.alicdn.com/tfs/TB166VWRLb2gK0jSZK9XXaEgFXa-1072-933.png)

至此，Java Web开发环境搭建完成。

​	

./startup.sh

./shutdown.sh

47.104.79.18:8081

:8080/sel/toLogin

netstat -ap |grep 8080 //查找tomcat端口是否被占用



tee /etc/docker/daemon.json <<-'EOF' {  "registry-mirrors": ["https://yb12hx1m.mirror.aliyuncs.com"] } EOF

tar -zxvf hadoop-2.7.6.tar.gz -C /opt/ mv /opt/hadoop-2.7.6 /opt/hadoop





sql 语句

CREATE TABLE `user` (
  `uid` int(11) NOT NULL AUTO_INCREMENT,
  `uname` varchar(50) NOT NULL,
  `password` varchar(20) DEFAULT NULL,
  `sex` varchar(10) DEFAULT NULL,
  `age` int(11) DEFAULT NULL,
  `adress` varchar(50) DEFAULT NULL,
  `headerPath` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`uid`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=latin1



CREATE TABLE `goods` (
  `gid` int(11) NOT NULL AUTO_INCREMENT,
  `gname` varchar(20) NOT NULL,
  `price` int(11) DEFAULT NULL,
  `counts` int(11) DEFAULT NULL,
  `uid` int(11) DEFAULT NULL,
  PRIMARY KEY (`gid`),
  KEY `g_u` (`uid`),
  CONSTRAINT `g_u` FOREIGN KEY (`uid`) REFERENCES `user` (`uid`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=latin1



# Hadoop

安装Hadoop

1. 执行以下命令，下载Hadoop安装包。

```
wget https://mirrors.tuna.tsinghua.edu.cn/apache/hadoop/common/hadoop-2.9.2/hadoop-2.9.2.tar.gz
```

2. 执行以下命令，解压Hadoop安装包至 /opt/hadoop。

```
tar -zxvf hadoop-2.7.6.tar.gz -C /opt/mv /opt/hadoop-2.9.2 /opt/hadoopecho 'export HADOOP_HOME=/opt/hadoop/' >> /etc/profileecho 'export PATH=$PATH:$HADOOP_HOME/bin' >> /etc/profileecho 'export PATH=$PATH:$HADOOP_HOME/sbin' >> /etc/profilesource /etc/profile    
```

3. 执行以下命令，修改配置文件yarn-env.sh 和 hadoop-env.sh。

```
echo "export JAVA_HOME=/root/java/jdk" >> /opt/hadoop/etc/hadoop/yarn-env.sh echo "export JAVA_HOME=/root/java/jdk" >> /opt/hadoop/etc/hadoop/hadoop-env.sh
```

4. 执行以下命令，测试Hadoop是否安装成功。

```
hadoop version
```

如果返回以下信息，则表示安装成功。




 配置Hadoop

1. 修改Hadoop配置文件core-site.xml。

  a. 执行以下命令开始进入编辑页面。

```
vim /opt/hadoop/etc/hadoop/core-site.xml
```

  b. 输入 i 进入编辑模式。

  c. 在<configuration></configuration>节点内插入如下内容。

```
<property>        <name>hadoop.tmp.dir</name>        <value>file:/opt/hadoop/tmp</value>        <description>location to store temporary files</description>    </property>    <property>        <name>fs.defaultFS</name>        <value>hdfs://localhost:9000</value>    </property>
```

  d. 按Esc键退出编辑模式，输入:wq保存退出。

2. 修改Hadoop配置文件 hdfs-site.xml。

  a. 执行以下命令开始进入编辑页面。

```
vim /opt/hadoop/etc/hadoop/hdfs-site.xml
```

  b. 输入 i 进入编辑模式。

  c. 在<configuration></configuration>节点内插入如下内容。

```
 <property>        <name>dfs.replication</name>        <value>1</value>    </property>    <property>        <name>dfs.namenode.name.dir</name>        <value>file:/opt/hadoop/tmp/dfs/name</value>    </property>    <property>        <name>dfs.datanode.data.dir</name>        <value>file:/opt/hadoop/tmp/dfs/data</value>    </property>
```



  d. 按Esc键退出编辑模式，输入:wq保存退出。



配置SSH免密登录

1. 执行以下命令，创建公钥和私钥。

```
ssh-keygen -t rsa
```

![img](https://img.alicdn.com/tfs/TB1shmeilBh1e4jSZFhXXcC9VXa-702-441.png)

2. 执行以下命令，将公钥添加到authorized_keys文件中。



```
cd .sshcat id_rsa.pub >> authorized_keys 启动Hadoop1.  执行以下命令，初始化namenode 。hadoop namenode -format2.  依次执行以下命令，启动Hadoop。start-dfs.shstart-yarn.sh3.  启动成功后，执行以下命令，查看已成功启动的进程。4.  打开浏览器访问http://<ECS公网IP>:8088 和 http://<ECS公网IP>:50070，显示如下界面则表示Hadoop伪分布式环境搭建完成。
```

### 上传LISENSE.txt

hdfs dfs -put LISENSE.txt /

### 删除文件LISENSE.txt

hdfs dfs -rm -r /LISENSE.txt



/opt/hadoop/share/hadoop/mapreduce    

yarn jar hadoop-mapreduce-examples-2.7.6.jar wordcount /LICENSE.txt /output01

hdfs dfs -cat/output01/part-r-00000



/root/hive/apache-hive-1.2.1-bin 



HIVE 表    按住 Ctrl +V+A 



192.168.159.66 node01

192.168.159.77 node02

192.168.159.88 node03
