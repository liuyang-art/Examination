# Examination
学生成绩管理系统
简介
 
这个项目是一个简单的教务查询系统，该练手小项目希望能帮助到大家，熟悉SSM的整合开发
使用技术
 
IOC容器：Spring
Web框架：SpringMVC ORM框架：Mybatis 安全框架：Shiro
数据源：C3P0 日志：log4j
前端框架：Bootstrap
快速上手
 
1、运行环境和所需工具
编译器：IntelliJ IDEA数据库：Mysql5
JDK版本：jdk1.8
Tomcat版本：Tomcat8.x
2、初始化项目
在你的Mysql中，创建一个数据库名称为 examination_system 的数据库，并导入我提供的 .sql 文件,
进入src/main/resources修改mysql.properties配置文件,把数据库登录名和密码，改为你本地的
使用 IntelliJ IDEA 导入项目
在 IntelliJ IDEA 中，配置我们的 Tomcat，启动运行

![image](https://user-images.githubusercontent.com/81675253/173782598-b7a2e08e-f17c-4e1e-ba5a-a03da71ebb59.png)










登录账户
管理员账户：admin 教师账户：1001
学生账户：10001 密码均为：123
功能模块介绍
 
1、登录模块功能
使用Shiro权限管理框架，实现登录验证和登录信息的储存，根据不同的登录账户，分发权限角色，对不同页面url进行角色设置
2、管理员模块功能
管理员可对 教师信息、学生信息、课程信息 进行 增删改查 操作，管理员账户，可以重置非管理员账户的密码
课程管理：当课程已经有学生选课成功时，将不能删除学生管理：添加学生信息时，其信息也会添加到登录表中教师管理：同上
账户密码重置：
 
修改密码：
![image](https://user-images.githubusercontent.com/81675253/173782802-2d3d3b09-2ef7-48ec-9828-d2a82715f8cb.png)























3、教师模块功能
教师登陆后，可以获取其，教授的课程列表，并可以给已经选择该课程的同学打分，无法对已经给完分  的同学进行二次操作
我的课程
 
修改密码
![image](https://user-images.githubusercontent.com/81675253/173782849-049bf33a-0e19-4450-98e7-741282917fa6.png)

















4、学生模块功能
学生登录后，根据学生信息，获取其已经选择的课程，和已经修完的课程
所有课程:  在这里选修课程，选好后，将会自动跳转到已选课程选项
已选课程:  这里显示的是，还没修完的课程，也就是老师还没给成绩，由于还没有给成绩，所以这里可以进行退课操作
已修课程: 显示已经修完，老师已经给成绩的课程
修改密码:
![image](https://user-images.githubusercontent.com/81675253/173782960-fdf9f106-f805-4dca-a399-92ab9609b3c8.png)

 ![image](https://user-images.githubusercontent.com/81675253/173782995-709b7373-d380-49ed-b288-dddeac2df734.png)

 
 
