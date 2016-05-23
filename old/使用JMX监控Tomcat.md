## 激活Tomcat的JMX远程配置

** 程序使用JMX监控Tomcat，需激活Tomcat的JMX远程配置，先修改Tomcat的启动脚本，windows下为bin/catalina.bat（linux下为catalina.sh），添加以下内容**

``` 
set JMX_REMOTE_CONFIG=-Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.port=8999 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false
set CATALINA_OPTS=%CATALINA_OPTS% %JMX_REMOTE_CONFIG% 
```

**要注意以上语句的位置不能太后面，可以加在【if "%OS%" == "Windows_NT" setlocal】一句后的大段的注释后面。**

**程序除了监控Tomcat是否正常运行，如果未部署XJPT项目同样视为异常。**



## 配置JavaMelody监控详细信息 (可选)

**若部署的XJPT非最新版本，还需：**

**在被监控项目web.xml中加入如下代码 **

``` 
<filter>   
        <filter-name>monitoring</filter-name>   
        <filter-class>net.bull.javamelody.MonitoringFilter</filter-class>   
</filter>   
<filter-mapping>   
        <filter-name>monitoring</filter-name>   
        <url-pattern>/*</url-pattern>   
</filter-mapping>   
<listener>   
        <listener-class>net.bull.javamelody.SessionListener</listener-class>   
</listener> 
```

**将javamelody.jar和jrobin-1.5.9.1.jar复制到被监控项目的LIB目录**