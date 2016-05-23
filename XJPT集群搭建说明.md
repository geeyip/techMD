# 搭建步骤 #

## 安装Apache与Tomcat ##
安装Apache2.2,使用默认设置,并且安装路径中不要空格。
安装Tomcat。

## 配置Apache ##
拷贝**mod_jk.so**到Apache安装路径的modules文件夹下
拷贝文件**mod_jk.conf**和**workers.properties**到Apache安装路径的conf文件夹下

修改Apache配置文件**httpd.conf**, 在最后一行末尾添加:
	
	include "D:\Apache2.2\conf\mod_jk.conf"
这里换成你正确的路径
Tomcat节点配置在workers.properties文件中，记得修改成正确的配置。

## 配置Tomcat ##
1.修改tomcat对应的service.xml文件,保证Apache对应的 workers.properties中的AJP13的connector的port. 


    <!-- 定义一个AJP 1.3 连接端口为9988 ,默认值为8009 -->
    <Connector port="9988" protocol="AJP/1.3" redirectPort="8443" />

如果同台机子多个tomcat，或默认端口8009被占用，就需要修改port。

2.增加jvmRoute的值,保证同workers.properties里边配置的值一致


    <!--增加jvmRoute,值为在Apache中配置的list集群结点中的值,这里定义为tomcat1结点-->
    <Engine name="Catalina" defaultHost="localhost" jvmRoute="tomcat1">

增加了jvmRoute属性，要和works.properties中的保持一致。

3.去掉默认注释掉的集群配置

    <!--取消集群结点相关的注释,该句默认值注释掉的,我们需要配置集群所以去掉注释,让其起作用-->
    <Cluster className="org.apache.catalina.ha.tcp.SimpleTcpCluster"/>

## 注意事项 ##
Apache的访问端口在httpd.conf中配置，默认为80
