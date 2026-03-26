## 引言：框架编程技术期末考试，一天快速突击，闪击及格线！开干：

### 轻量级 JavaWeb 开发组合框架有哪些？⭐

答：轻量级 Java Web 开发框架通常注重简洁、高效和易于使用，适合快速开发中小型应用。以下是一些常见的轻量级 Java Web 开发组合框架： 老师主要讲了三种比较常见的整合开发的框架：

1. Spring Boot + Thymeleaf， 引擎模板来实现简单的案例，比如商品信息的修改还有员工信息表的增删改查，就是通过前端模板引擎调用接口控制层的接口实现的。不仅如此springboot应用的的初始搭建和开发过程，还内置了Tomcat服务器方便快捷。
2. springboot+jsp； 虽然现在jsp不常用甚至快被淘汰了，但是传统的jsp页面和java’web开发技术适合熟悉的jsp开发者。
3. Spring Boot + Thymeleaf + MyBatis 三者整合的页面也有相应的案例。
4. 剩下的像模板引擎加JPA/Hibernate， springboot加模板引擎加JPA，MongDb都没有讲到。

### 在 Maven 环境中配置本地仓库，则应在 maven 安装路径下 conf 文件夹中的 Settings.xml 文件中添加哪些标签来设置本地仓库和中央仓库。⭐⭐

答：这是老师第一节课讲的内容：就是需要在Maven环境下配置的，这个很简单，咱们本地仓库有一个setting.xml的文件，在这个文件中添加相关标签：

```
<settings>
  <!-- 配置本地仓库路径 -->
  <localRepository>/E:/repository</localRepository>
</settings>

```

这里的路径就是本地仓库路径，idea中默然加载的就是这个路径的，也可以指定本地仓库的路径。你可以将路径设置为任何你希望的位置。一般老师出题不会问这么细大致了解一下即可。

除此之外还要配置中央仓库：

```
<settings>
  <!-- 配置中央仓库 -->
  <mirrors>
    <mirror>
      <id>central</id>
      <mirrorOf>central</mirrorOf>
      <url>https://repo.maven.apache.org/maven2</url>
    </mirror>
  </mirrors>
</settings>

```

```
<mirrors>：定义镜像仓库。

<mirror>：定义一个镜像仓库。

<id>：镜像仓库的唯一标识。

<mirrorOf>：指定要镜像的仓库。central 表示中央仓库。

<url>：镜像仓库的 URL。

```

### maven环境下的创建的项目可以选择那些模板？⭐⭐

IntelliJ IDEA 环境中创建的 Maven 项目的流程，特别是原型模板选择 Java 项目：`org.apache.maven.archetypes:maven-archetype-quickstart` JavaWeb 项目：`org.apache.maven.archetypes:maven-archetype-webapp` 多模块项目父模块：`org.apache.maven.archetypes:maven-archetype-site-simple` 以上三类原型模板的项目分别默认的打包方式（jar, war,）  
**咱们用的最多的模板就是quickstart-是java项目**

### JSP 页面代码是那两种代码组成？？⭐

答：其实`JSP`页面是由两种代码组成的；分别是`静态内容`和`动态内容`；静态内容就是咱们耳熟能详的`HTML`、`CSS`和`js`三剑客了；页面加载的时候不会变化，属于静态的；而动态内容通常是嵌入在JSP页面中的JAVA代码，根据请求参数、数据库查询结果等动态生成内容。

一个简单的实例，没时间的同学不用看直接跳过：

```
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
    <title>JSP 页面示例</title>
</head>
<body>
    <h1>欢迎来到 JSP 页面</h1>
    <%-- 动态内容 --%>
    <%
        String name = request.getParameter("name");
        if (name == null) {
            name = "Guest";
        }
    %>
    <p>你好, <%= name %>!</p>
</body>
</html>

```

一句话：**静态内容：HTML 结构和样式。  
动态内容：嵌入的 Java 代码，根据请求参数动态生成内容。**

### 常用 lombok 注解及其功能(Set 方法，Get 方法，无参构造方法和全参构造方法)

答： 这个其实需要我们在`pom.xml` 全局配置文件中加载lombock的依赖，还需要在idea中的setting选项下的`plugin`  
下配置相关插件，一个🌶辣椒的插件；他的`@Getter`和`@Setter` lombock注解专属的两个注解，他自动生成相对应的set和get方法对属性进行封装对外提供接口用于调用内部的属性修改等…还有`@NoArgsConstructor`自动生成无参构造，还有`@AllArgsConstructor`自动生成全参构造。如果说这些注解都不想用直接用暴力的，`@Data`注解自动生成全部的set，get，无参有参构造的全部方法。

## Spring部分的考点⭐⭐⭐

### Spring 基本用法需要添加的基础依赖

答：这哥们的一个核心的依赖就是`Spring Core`，这哥们提供了`spring`框架的核心功能，`Core`这个单词的意思就是核心的意思，这个依赖还包括依赖注入`（DI）` 和控制反转`（IOC）`  
要说具体代码的话就是pom文件的那个

```
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-core</artifactId>
    <version>5.3.10</version>
</dependency>

```

还有一个兄弟依赖 `Spring Context`功能提供Spring应用上下文，支持Bean的配置和管理；

```
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>5.3.10</version>
</dependency>

```

还有一个特别重要的：`Spring Beans` 这哥们是提供 `Spring Bean` 的定义和管理功能。

```
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-beans</artifactId>
    <version>5.3.10</version>
</dependency>

```

以上是 Spring 基本用法中常用的基础依赖。根据项目需求，可以选择性地添加这些依赖。通常情况下，`spring-core、spring-context 和 spring-beans` 是必须的，其他依赖根据具体功能需求添加。 当然还有很多，像：`Spring AOP`、`Spring Web`等等 ，考试不会考这么多，有兴趣了解即可。

### Spring 基本用法（参照课堂实验 3） （1）依赖注入：ApplicationContext.xml 实现依赖注入 设值注入（类中要有 Setter 方法） 构造注入（类中要有带参数的构造方法）

答：说白了这个设值注入就是通过类的`Setter`方法将依赖注入到对象中；比如在业务逻辑处理层`UserService`类中有一个`setUserDao`的方法，和一个`saveUser()`方法，然后userdao类有一个save的方法；`ApplicationContext.xml`应用上下文的这个xml文件就可以用

```
<bean id="userDao" class="com.example.UserDao"/>

    <!-- 配置 UserService Bean，并使用设值注入 -->
    <bean id="userService" class="com.example.UserService">
        <property name="userDao" ref="userDao"/>

```

紧接着用创建一个Main类通过`ClassPathXmlApplicationContext`这个对象把配置文件xml传进来，返回一个`context`直接调用`getbean`方法，把业务逻辑处理层的`userService`类传进来，调用`saveUser`方法；这个地方有点绕，贼坑；

* 第二种就是构造注入了；这哥们其实就是通过类的构造方法将依赖注入到对象中；

```
<!-- 配置 UserDao Bean -->
    <bean id="userDao" class="com.example.UserDao"/>

    <!-- 配置 UserService Bean，并使用构造注入 -->
    <bean id="userService" class="com.example.UserService">
        <constructor-arg ref="userDao"/>

```

```
 <constructor-arg ref="userDao"/>  是构造注入的核心

```

一句话：  
**设值注入：通过类的 Setter 方法将依赖注入到对象中。  
构造注入：通过类的构造方法将依赖注入到对象中。**

### （2）控制反转：在主类测试类中，创建控制反转容器，获取 bean 实例，实现 bean 实例 具有的功能。（重点理解标红的代码）⭐⭐

答： 控制反转这个哥们就是Spring 框架的核心概念之一，它将对象的创建和管理交给 Spring 容器，而不是由开发者手动创建和管理。通过控制反转，开发者可以专注于业务逻辑，而不必关心对象的创建和依赖管理。这么长考试不用背下来，写关键代码就好了：

比如如果考试出了要知道， 举个例子：

```
import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class Main {
    public static void main(String[] args) {
        // 创建控制反转容器，加载 Spring 配置文件
        ApplicationContext context = new ClassPathXmlApplicationContext("ApplicationContext.xml");

        // 获取 UserService Bean 实例
        UserService userService = context.getBean("userService", UserService.class);

        // 调用 UserService 的功能方法
        userService.saveUser();
    }
}

```

把实例的Bean 这一行代码去掉填空：

```
// 获取 UserService Bean 实例
        UserService userService = context.getBean("userService", UserService.class);

        // 调用 UserService 的功能方法
        userService.saveUser();

```

这两句是关键代码，就是直接用userService 直接调用他的saveUser方法；  
UserService.java的代码：

```
public class UserService {
    public void saveUser() {
        System.out.println("User saved!");
    }
}

```

ApplicationContext.xml

```
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!-- 配置 UserService Bean -->
    <bean id="userService" class="com.example.UserService"/>
</beans>

```

### 3. AOP （1）AOP 基本概念（切面 连接点 增强处理 代理对象） （2）基于代理类的 AOP 实现（重点代理 Bean 元素的声明）⭐⭐⭐

一句话：

**AOP 基本概念：切面、连接点、增强处理、切入点、代理对象。  
基于代理类的 AOP 实现：定义目标类、切面类，配置 Spring 容器，启用 AOP 自动代理。**

考填空题的话就是考AOP的基本概念：

1. 切面（Aspect）：横切关注点的模块化，包含增强处理和切入点。  
   **2. 连接点（Join Point）：程序执行过程中的一个点，如方法调用。**
2. 增强处理（Advice）：在特定连接点执行的代码，如前置、后置、环绕等。  
   **4. 切入点（Pointcut）：连接点的集合，定义哪些连接点应用增强处理。**
3. 代理对象（Proxy Object）：目标对象的代理，用于执行增强处理。

```
<!-- 配置目标类 bean -->
 <bean id="myTestDao" class=" spring.demo.dao.impl.TestDaoImpl"/>
 <!-- 配置切面类 bean -->
  <bean id="myAspect" class="spring.demo.interceptor.MyAspect" /> <!-- 使用 Spring 代理工厂定义一个名为 testDaoProxy 的代理 --> 
  <bean id="testDaoProxy" class="org.springframework.aop.framework.ProxyFactoryBean"> <!-- 指定代理实现的接口-->
   <property name="proxyInterfaces" value=" spring.demo.dao.TestDao" /> 
   <!-- 指定目标对象 --> 
   <property name="target" ref="myTestDao" /> 
   <!-- 指定切面，织入环绕通知-->
    <property name="interceptorNames" value="myAspect"/> <!-- 指定代理方式，true 指定 CGLIB 动态代理，false 指定 JDK 动态代理 --> 
    <property name="proxyTargetClass" value="true"/> </bean>

```

重点理解

```
<property name="proxyInterfaces" value=" spring.demo.dao.TestDao" />

```

和

```
<property name="target" ref="myTestDao" />

```

考试就考这两句，换一下模子；

举个更简单的例子：  
定义一个`UserService`的类，有一个`saveUser`方法

```
public class UserService {
    public void saveUser() {
        System.out.println("User saved!");
    }
}

```

定义切面类：`LoggingAspect`有一个`logBefore`方法

```
import org.aspectj.lang.annotation.Aspect;
import org.aspectj.lang.annotation.Before;

@Aspect
public class LoggingAspect {
    @Before("execution(* com.example.UserService.saveUser(..))")
    public void logBefore() {
        System.out.println("Before saving user...");
    }
}

```

然后配置 Spring 容器`ApplicationContext.xml`配置`bean`和`AOP`代理

```
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:aop="http://www.springframework.org/schema/aop"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd
                           http://www.springframework.org/schema/aop
                           http://www.springframework.org/schema/aop/spring-aop.xsd">

    <!-- 配置 UserService Bean -->
    <bean id="userService" class="com.example.UserService"/>

    <!-- 配置 LoggingAspect Bean -->
    <bean id="loggingAspect" class="com.example.LoggingAspect"/>

    <!-- 启用 AOP 自动代理 -->
    <aop:aspectj-autoproxy/>
</beans>

```

最后直接在Main测试类中调用`userServie`的`saveUser`方法

```
import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class Main {
    public static void main(String[] args) {
        ApplicationContext context = new ClassPathXmlApplicationContext("ApplicationContext.xml");
        UserService userService = context.getBean("userService", UserService.class);
        userService.saveUser();
    }
}

```

## C、SpringBoot 部分 （重中之重）⭐⭐⭐⭐⭐

1. Spring Boot 提供的实现对 RESTful 接口的支持的常用注解及其功能

`@Controller:`这哥们是标识一个类位控制类，用于处理HTTP请求。  
`@RequestBody:`将HTTP请求体中的数据绑定到方法参数。  
`@ResponseBody：`将方法返回值作为 HTTP 响应体返回。  
`@RestController：`组合 `@Controller @ResponseBody，`用于构建 RESTful Web 服务。就是可以这么理解。  
`@RequestMapping：`映射 HTTP 请求到控制器方法，支持路径、请求方法、请求参数等配置。

### 2. 接口数据校验中定义实体（Bean）类，配置校验规则使用的常用注解⭐⭐⭐⭐

`@NotNull：`验证属性值不能为空。

`@NotEmpty：`验证集合、字符串或数组不能为空。

`@NotBlank：`验证字符串不能为空且不能只包含空白字符。

`@Min` 和 `@Max`：验证数值的最小值和最大值。

`@Size`：验证集合、字符串或数组的大小范围。

`@Past` 和 `@Future`：验证日期是否在过去或未来。

举个例子 更直观一点，请看代码！：

```
import javax.validation.constraints.Min;
import javax.validation.constraints.NotBlank;
import javax.validation.constraints.NotNull;
import javax.validation.constraints.Size;

public class User {
    @NotNull(message = "ID 不能为空")
    private Long id;

    @NotBlank(message = "用户名不能为空")
    @Size(min = 3, max = 20, message = "用户名长度必须在 3 到 20 之间")
    private String username;

    @Min(value = 18, message = "年龄必须大于等于 18")
    private int age;

    // Getter 和 Setter 方法
}

```

### 文件上传（重点单文件上传）⭐⭐⭐⭐

```
enctype="multipart/form-data"

```

这句代码必考！

接口控制层：实现文件上传方法的参数类型

```
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.multipart.MultipartFile;

@RestController
public class FileUploadController {

    @PostMapping("/upload")
    public String uploadFile(@RequestParam("file") MultipartFile file) {
        if (file.isEmpty()) {
            return "文件为空";
        }

        // 获取上传文件的原始文件名
        String originalFilename = file.getOriginalFilename();

        // 保存文件到服务器
        try {
            file.transferTo(new File("/path/to/save/" + originalFilename));
            return "文件上传成功";
        } catch (IOException e) {
            e.printStackTrace();
            return "文件上传失败";
        }
    }
}

```

```
 String originalFilename = file.getOriginalFilename();

```

这句代码必考；

### 定时任务设置使用的 @Scheduled 注解中的 cron 表达式表示规则⭐⭐⭐⭐

答：在 Spring Boot 中，`@Scheduled` 注解用于配置定时任务。`cron` 表达式是一种强大的时间表达式，用于指定定时任务的执行时间。以下是 cron 表达式的详细规则：

`cron` 表达式格式  
`cron` 表达式由 6 或 7 个字段组成，每个字段之间用空格分隔：

> 秒 分 时 日 月 周 [年]

* 秒（0-59）
* 分（0-59）
* 时（0-23）
* 日（1-31）
* 月（1-12 或 JAN-DEC）
* 周（1-7 或 SUN-SAT）
* 年（可选，1970-2099）

`*`表示所有可能的值。例如，\* 在分字段表示每分钟。

`,`表示枚举值。例如，1,3,5 在秒字段表示第 1、3、5 秒。

`-`表示范围。例如，1-5 在秒字段表示第 1 到 5 秒。

`/`表示增量。例如，0/15 在秒字段表示从第 0 秒开始，每 15 秒一次。

`?`表示无特定值，用于日和周字段，避免冲突。

`L`表示最后，用于日和周字段。例如，L 在日字段表示当月的最后一天。

`W`表示工作日，用于日字段。例如，15W 表示离 15 号最近的工作日。

`#`表示第几周的第几天，用于周字段。例如，6#3 表示第 3 个周五。

示例：  
**每分钟执行一次：**

```
0 * * * * *

```

每小时的第 15 分钟执行一次：

```
0 15 * * * *

```

每天的 10:15 执行一次：

```
0 15 10 * * *

```

每周一的 10:15 执行一次：

```
0 15 10 ? * MON

```

每月的最后一天的 23:59 执行一次：

```
0 59 23 L * ?

```

每月的第 1 个工作日的 9:00 执行一次：

```
0 0 9 1W * ?

```

举一个实例：使用 `@Scheduled` 注解配置定时任务：  
定义一个方法，添加注解`0 15 10 * * ?` 表示每天上午 10:15 执行一次定时任务。

```
import org.springframework.scheduling.annotation.Scheduled;
import org.springframework.stereotype.Component;

@Component
public class MyScheduledTask {

    @Scheduled(cron = "0 15 10 * * ?")
    public void doTask() {
        System.out.println("定时任务执行...表示每天上午 10:15 执行一次定时任务。");
    }
}

```

## SpringBoot+MyBatista 框架整合部分（参照最后课堂实验 8+最后大作业） ⭐⭐⭐⭐⭐⭐

答：这部分的分值占百分之60％

主要就是`dao-service-controller` 三层架构搞清楚了这里问题不大：  
还有sql语句要熟练

举一个最简单的代码示例完整结束这一个大问题：

新建一个Entity包下的实体类User，实体类属性名与数据库中的数据表名和字段名对应。

User.java

```
public class User {
    private Long id;
    private String username;
    private String password;

    // Getter 和 Setter 方法
}

```

Mapper 层：UserMapper.xml 及其接口

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
  PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
  "http://mybatis.org/dtd/mybatis-3-mapper.dtd">

<mapper namespace="com.example.mapper.UserMapper">
    <insert id="insertUser" parameterType="com.example.entity.User">
        INSERT INTO users (username, password) VALUES (#{username}, #{password})
    </insert>

    <select id="selectUserById" parameterType="long" resultType="com.example.entity.User">
        SELECT * FROM users WHERE id = #{id}
    </select>

    <update id="updateUser" parameterType="com.example.entity.User">
        UPDATE users SET username = #{username}, password = #{password} WHERE id = #{id}
    </update>
</mapper>

```

UserMapper.java

```
import org.apache.ibatis.annotations.Mapper;
import com.example.entity.User;

@Mapper
public interface UserMapper {
    void insertUser(User user);
    User selectUserById(Long id);
    void updateUser(User user);
}

```

Service 层：接口及其接口实现类如何向映射层转发指令

```
public interface UserService {
    void saveUser(User user);
    User getUserById(Long id);
    void updateUser(User user);
}

```

UserServiceImpl.java

```
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;
import com.example.entity.User;
import com.example.mapper.UserMapper;

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    private UserMapper userMapper;

    @Override
    public void saveUser(User user) {
        userMapper.insertUser(user);
    }

    @Override
    public User getUserById(Long id) {
        return userMapper.selectUserById(id);
    }

    @Override
    public void updateUser(User user) {
        userMapper.updateUser(user);
    }
}

```

Controller 层  
UserController.java

```
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.*;
import com.example.entity.User;
import com.example.service.UserService;

@RestController
@RequestMapping("/users")
public class UserController {

    @Autowired
    private UserService userService;

    @PostMapping
    public String saveUser(@RequestBody User user) {
        userService.saveUser(user);
        return "用于信息保存成功";
    }

    @GetMapping("/{id}")
    public User getUserById(@PathVariable Long id) {
        return userService.getUserById(id);
    }

    @PutMapping
    public String updateUser(@RequestBody User user) {
        userService.updateUser(user);
        return "用于信息更新成功！";
    }
}

```

模板文件的编辑文件  
前端的user.html

```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>User List</title>
</head>
<body>
    <h1>User List</h1>
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Username</th>
                <th>Password</th>
            </tr>
        </thead>
        <tbody>
            <tr th:each="user : ${users}">
                <td th:text="${user.id}"></td>
                <td th:text="${user.username}"></td>
                <td th:text="${user.password}"></td>
            </tr>
        </tbody>
    </table>
</body>
</html>

```

注意这里的`<tr th:each="user : ${users}"> 中的 user 和 ${users}`

```
${users}
含义：${users} 是一个 Thymeleaf 表达式，用于从模型（Model）中获取名为 users 的属性值。

类型：users 通常是一个集合（如 List、Set 等），包含多个对象（如 User 对象）。

示例：假设在控制器中，你将一个 List<User> 对象添加到模型中，并命名为 users。

```

```
@GetMapping("/users")
public String getUsers(Model model) {
    List<User> users = userService.getAllUsers();
    model.addAttribute("users", users);
    return "user";
}

```

th:each 属性  
含义：th:each 是 Thymeleaf 的一个迭代属性，用于遍历集合中的每个元素。

语法：th:each="item : collection"，其中item是迭代变量，{collection}"，其中 item 是迭代变量，collection"，其中item是迭代变量，{collection} 是要遍历的集合。

作用：遍历集合中的每个元素，并将每个元素绑定到 item 变量上。

3. user  
   含义：user 是迭代变量，表示集合中的每个元素。

类型：user 的类型与集合中元素的类型相同（如 User 对象）。

作用：在每次迭代中，user 变量将引用集合中的一个元素，可以在模板中使用该变量来访问元素的属性。

```
<tbody>
            <!-- 遍历 users 集合，将每个 user 对象绑定到 user 变量 -->
            <tr th:each="user : ${users}">
                <td th:text="${user.id}"></td>
                <td th:text="${user.username}"></td>
                <td th:text="${user.password}"></td>
            </tr>
        </tbody>

```

最后的最后就是配置文件了`application.properties`

```
# 数据源设置
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=root
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# 映射文件所在位置
mybatis.mapper-locations=classpath:mapper/*.xml

# 实体类所在的包设置
mybatis.type-aliases-package=com.example.entity

```

## 总结

* Entity 层：实体类属性名与数据库字段名对应。

  Mapper 层：XML 映射文件和接口，实现插入、查询、修改等数据库操作。

  Service 层：接口和实现类，向映射层转发指令。

  Controller 层：处理 HTTP 请求，调用服务层方法，返回页面或数据。

  模板文件：Thymeleaf 模板，展示数据。

  配置文件：配置数据源、映射文件位置、实体类包等。

> 人类学会走路，也得学会摔跤，而且只有经过摔跤他才能学会走路。——马克思