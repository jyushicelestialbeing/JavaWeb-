# JavaWeb学习笔记
## tomcat配置
   - 可以在conf/server.xml下配置端口，默认为8080
   - bin/shutdown.sh 关闭服务 bin/startup.sh开启服务
   - webapps下存放项目，需压配合web.xml进行部署
   - 需要在/etc/profile下配置环境变量
      ```
      # tomcat
      export CATALINA_HOME=/opt/tomcat/你的tomcat根目录
      export CLASSPATH=.:$JAVA_HOME/lib:$CATALINA_HOME/lib
      export PATH=$PATH:$CATALINA_HOME/bin
      # end
      ```
## Servlet配置
   - 配置好tomcat后可以在idea中创建tomcat项目，idea会自动创建好相关环境
   - src目录下可以直接放类文件代码
   - web/WEB-INF下存放web.xml配置文件
   - 但是要注意，最终运行的文件会在运行前编译到out文件夹中,out/artifacts/xxxxx/WEB-INF下存放运行的web.xml
   - 127.0.0.1:端口号/xxxxx/你的类映射名 用于访问你的Servlet类，而不是很多教程中 127.0.0.1：端口号/类名 这样会404
   - 不需要自己在项目中创建classes和lib文件夹
## Servlet使用
   - 导入Servlet接口
      ```java
      import javax.servlet.*;
      ```
   
