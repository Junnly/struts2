# struts2

struts概念：是流行和成熟的基于MVC设计模式的web应用程序框架
      使用的目的：为了帮助我们减少在运用MVC设计模型来开发web应用的时间
MVC概念：是模型视图控制器（model view Controller),一种软件设计典范，用于一种业务逻辑，数据，界面显示分离的方法组织代码，
         将业务逻辑聚集到一个部件里面，在改进和个性化定制界面以及用户交互的同时，不需要重新编写代码。

JSP+Serclet+JavaBean = model2
 
 配置要求：Servlet API 2.4；JSP API 2.0；JAVA 5
 搭建struts2环境步骤：下载JAR包，创建web项目，创建并完善相关配置文件，创建Action并测试启动。
 jar包下载：http://struts.apache.org/
           http：//people。apache.org/builds/struts/
           
 Action 的搜索顺序：
        eg:http://localhost:8080/struts2/path1/path2/path3/student.action
        第一步：判断package是否存在，如：path1/path2/path3/
        如果存在：第二步：判断action是否存在，如果不存在则取默认的namespace的package里面寻找action
                 第三步：如果没有，则报错。
        如果不存在：第二步：检查上已经路径的package是否存在(直到namespace),重复第一步
                   第三步：如果没有，则报错。
                   
  Struts工作流程：   MVC:view ---jsp
                        Controller -- ActionServlet
                        Model----ActionForm
                        
                request出现的时候，通过各层filter过滤器分发请求， 通过Action找到可以实现的
