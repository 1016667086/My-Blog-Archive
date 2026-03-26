Description:

An attempt was made to call a method that does not exist. The attempt was made from the following location:

```
org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration$EnableWebMvcConfiguration.welcomePageHandlerMapping(WebMvcAutoConfiguration.java:453)

```

The following method did not exist:

```
org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration$EnableWebMvcConfiguration.getInterceptors()[Ljava/lang/Object;

```

The method’s class, org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration$EnableWebMvcConfiguration, is available from the following locations:

```
jar:file:/C:/apache-maven-3.6.3/repository_lkd/org/springframework/boot/spring-boot-autoconfigure/2.1.8.RELEASE/spring-boot-autoconfigure-2.1.8.RELEASE.jar!/org/springframework/boot/autoconfigure/web/servlet/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class

```

The class hierarchy was loaded from the following locations:

```
org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration.EnableWebMvcConfiguration: file:/C:/apache-maven-3.6.3/repository_lkd/org/springframework/boot/spring-boot-autoconfigure/2.1.8.RELEASE/spring-boot-autoconfigure-2.1.8.RELEASE.jar
org.springframework.web.servlet.config.annotation.DelegatingWebMvcConfiguration: file:/C:/apache-maven-3.6.3/repository_lkd/org/springframework/spring-webmvc/5.3.23/spring-webmvc-5.3.23.jar
org.springframework.web.servlet.config.annotation.WebMvcConfigurationSupport: file:/C:/apache-maven-3.6.3/repository_lkd/org/springframework/spring-webmvc/5.3.23/spring-webmvc-5.3.23.jar

```

Action:

Correct the classpath of your application so that it contains a single, compatible version of org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration$EnableWebMvcConfiguration

Process finished with exit code 1

\*\*> 解决办法  
把pom文件里边的依赖包全部删掉，然后重新clean 一下

> 进行以下步骤来解决这个问题：
>
> 1. 确定并统一版本 请确认你的Spring Boot项目使用了一致的版本配置。最好使用spring-boot-starter-parent来统一管理版本。修改pom.xml中的parent和dependencies标签，确保没有其他版本号混入。
>
> 示例pom.xml配置：
>
> org.springframework.boot
> spring-boot-starter-parent
> 2.5.3 并检查所有的Spring Boot相关依赖是否去除了标签，例如：
> org.springframework.boot
> spring-boot-starter-web
> 2. 检查和清理 运行mvn dependency:tree命令来检查项目中的依赖关系树，注意是否有不兼容或者多版本的依赖存在。
>
> 确保.m2/repository目录的相关库没有损坏。由于你已经尝试删除了整个repository，这步可能不必要。
>
> 3. 重新构建 重新构建项目：mvn clean install。 确保Maven下载了所有正确的依赖包。
> 4. 运行和测试 重新启动你的Spring Boot应用。 观察是否还有类似的错误出现。
> 5. 追踪和验证 如果错误依然存在并且步骤1到步骤4都没有问题，建议检查是否有其他地方（如IDE设置、环境变量等）对classpath或依赖版本产生影响，或者是否有某些未在Maven管理下的库被错误引用。
>
> 此外，如果项目之前使用过其他版本的Spring  
> Boot，有可能某些配置上的更改需求没被应用，或是代码中存在一些与新版本不兼容的实现。这就需要根据具体的编码和配置，逐一检查。\*\*