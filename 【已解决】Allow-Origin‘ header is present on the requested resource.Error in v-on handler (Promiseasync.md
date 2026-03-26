## 项目场景：

今天在写vue加springboot技术编写前后端分离项目过程中出现了跨域问题，然而也花费了一些时间去找解决方法，csdn上面的大佬只能说太强了，虽然说的都挺有道理的，但是终究还是太弱了看不懂，后来自己琢磨了以下，想了想会不会是后端跨域请求出现了问题。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/b50e793ce9a731893a85a99c9d6355bd.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/df14e8fc7b0f65ea6ea12a1b3a0f2616.png)

## 问题描述：

```
Access to XMLHttpRequest 
at 'http://localhost:9000/userstate?id=1&state=true' f
rom origin 'http://localhost:8080' has been blocked 
by CORS policy: No 'Access-Control-Allow-Origin'
 header is present on the requested resource.
found in

---> <ElSwitch> at packages/switch/src/component.vue
       <ElTableBody>
         <ElTable> at packages/table/src/table.vue
           <ElCard> at packages/card/src/main.vue
             <UserList> at src/components/admin/UserList.vue
               <ElMain> at packages/main/src/main.vue
                 <ElContainer> at packages/container/src/main.vue... (1 recursive calls)
                   <Home> at src/components/Home.vue
                     <App> at src/App.vue
   
                       <Root>
                       Error: Request failed with status code 400
    at createError (createError.js?2d83:16)
    at settle (settle.js?467f:17)
    at XMLHttpRequest.handleLoad

```

## 原因分析：

跨域请求出现了问题，代码肯定有问题，需要改动。

## 解决方案：

后来我找到了 java后台 util包下的WebConfig配置类

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d86f2c1f4cd948d8592c600f019a6aa5.png)  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/c1a689eed46edeed65d04c3e47b5f99a.png)

找到了跨域的方法，果然没有加put 请求方式。

```
 @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**")
                .allowedOrigins("Http://localhost:8080","null")
                .allowedMethods("GET","POST","OPTION","DELETE")
                .allowCredentials(true)
                .maxAge(3600);
    }

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/f142adb021a45e06909d1eaf41ef977a.png)  
于是乎问题得以解决。前端vue 中也实现了相应的变化  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/7277652a2a38d83b3d65db6060427181.png)  
成功的修改了状态，实现了数据库的交互。

## 总结

一般跨域问题都应该检查一下自己前后端分离的项目中**后台** 的代码问题，看看是不是 @Configuration 配置类没有写还是 addCorsMappings方法中 请求方式没有写全。再或者 是 @CrossOrigin 注解 写错位置了。

**反正我是这样解决的，你的错误解决了吗？**