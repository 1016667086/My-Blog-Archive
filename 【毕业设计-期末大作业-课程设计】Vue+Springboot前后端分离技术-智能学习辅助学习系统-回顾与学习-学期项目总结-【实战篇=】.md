## 源码：

**前端Vue**：通过网盘分享的文件：springboot智能辅助系统后端代码.rar等2个文件  
 链接: https://pan.baidu.com/s/11WOqjwt6FOGq93R\_qgx0QQ?pwd=pd62 提取码: pd62  
 –来自百度网盘超级会员v2的分享

**后端Springboot**：通过网盘分享的文件：springboot智能辅助系统后端代码.rar等2个文件  
 链接: https://pan.baidu.com/s/11WOqjwt6FOGq93R\_qgx0QQ?pwd=pd62 提取码: pd62  
 –来自百度网盘超级会员v2的分享  
 源码传送门

## 前言

### 学习完黑马的实战项目总结回顾一下加深一下印象；也算这学期给自己的一个交代吧

## 一、运行效果前后端展示

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/607bb4cd65274850b28e3cba6d042026.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/642bcd6c7adb45438aa4026f665b03f8.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/319a59307f314242bd678729abb9f82a.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/70cdec6a98274f5eb0f2b2f7fd6ba4d7.png)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9deaf6b2dc3d462cb249ff969b54ea6b.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3e0f5e3271e1468990499139d71e67ba.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/538fca417913445cb461d38d06676189.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f18a24f66f044ba4a953c875f1d5728f.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/72c9bde4f55b4c56aa10b2aa2faf5ea2.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0e3575415cd64937be5ecfdef7186a09.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cb01f03c7a8f47fe99cde518972d1889.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6f95c8cb13ad4b5a987e1fded1989c99.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a58f922c2a924ad292c5b902c1f8e5cd.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b98471a87d3e4b0f8f388f03bd9905b7.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1a0cb5c2518548b188a5d3648556e74b.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/95569695ef664438b1f946727f5112a1.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8594e606bf5c4116aae0f90cc5adb964.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/80d760bcd9c945b6a701e8c9d32d0cca.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/12ac33f326c64b6a9d1ac62e03d5c4ac.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f18e4b8cc68647d99446b266ae271043.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4cc48d15917e47c7bb056d9343b9851e.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ca7f3d7d91174ff69c079d1604ae70c6.png)

## 二、具体实现步骤逻辑

Vue工程化的基础内容、TS、ElementPlus，那接下来呢，我们要通过一个案例，加强大家对于Vue项目的理解，并掌握Vue项目的开发 **部门管理** 和 **员工管理** 的功能开发

* 前后端分类开发
* 准备工作
* 页面布局
* Vue-Router
* 部门管理

我们介绍过，现在的企业项目开发有2种开发模式：**前后台混合开发**和**前后台分离开发**。

前后台混合开发，顾名思义就是前台后台代码混在一起开发。这种开发模式有如下缺点：

* 沟通成本高：后台人员发现前端有问题，需要找前端人员修改，前端修改成功，再交给后台人员使用
* 分工不明确：后台开发人员需要开发后台代码，也需要开发部分前端代码。很难培养专业人才
* 不便管理：所有的代码都在一个工程中
* 难以维护：前端代码更新，和后台无关，但是需要整个工程包括后台一起重新打包部署。

所以目前基本都是采用的前后台分离开发方式，如下图所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/db2e3d80b34345ba88669375485558a6.png)

我们将原先的工程分为前端工程和后端工程这2个工程，然后前端工程交给专业的前端人员开发，后端工程交给专业的后端人员开发。

前端页面需要数据，可以通过发送异步请求，从后台工程获取。但是，我们前后台是分开来开发的，那么前端人员怎么知道后台返回数据的格式呢？后端人员开发，怎么知道前端人员需要的数据格式呢？

所以针对这个问题，我们前后台统一制定一套规范！我们前后台开发人员都需要遵循这套规范开发，这就是我们的**接口文档**。接口文档有离线版和在线版本，接口文档示可以查询今天提供**资料/接口文档**里面的资料。

那么接口文档的内容怎么来的呢？是我们后台开发者根据产品经理提供的产品原型和需求文档所撰写出来的，产品原型示例可以参考今天提供**资料/页面原型**里面的资料。

那么基于前后台分离开发的模式下，我们后台开发者开发一个功能的具体流程如何呢？如下图所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c82701ee4fce4c91835718055d7e45c0.png)

1. 需求分析：首先我们需要阅读需求文档，分析需求，理解需求。
2. 接口定义：查询接口文档中关于需求的接口的定义，包括地址，参数，响应数据类型等等
3. 前后台并行开发：各自按照接口文档进行开发，实现需求
4. 测试：前后台开发完了，各自按照接口文档进行测试
5. 前后段联调测试：前段工程请求后端工程，测试功能

### 2. 准备工作

#### 2.1 创建Vue项目

在自己工作目录下，运行 `cmd` 打开命令行，运行如下指令，来创建vue项目![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2518cf5c392b48d1ac0f88d1ac1488f2.png)

#### 2.2 安装依赖

1). 在命令行中执行如下命令，为创建好的Vue项目安装 `ElementPlus、Axios` 的依赖。

```
npm install element-plus --save

npm install axios

```

2). 为创建好的 Vue项目 配置ElementPlus (参照官网)，在 `main.ts` 中引入如下配置信息 【注意：是追加如下内容】:

```
import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
import zhCn from 'element-plus/dist/locale/zh-cn.mjs'
import * as ElementPlusIconsVue from '@element-plus/icons-vue'

//引入ElementPlus的Icon组件
for (const [key, component] of Object.entries(ElementPlusIconsVue)) {
  app.component(key, component)
}
app.use(ElementPlus, {locale: zhCn})

app.mount('#app')

```

最终完整的 `main.ts` 文件内容如下：

```
import { createApp } from 'vue'
import { createPinia } from 'pinia'

import App from './App.vue'
import router from './router'
import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
import './assets/main.css'

import zhCn from 'element-plus/dist/locale/zh-cn.mjs'
import * as ElementPlusIconsVue from '@element-plus/icons-vue'

const app = createApp(App)

for (const [key, component] of Object.entries(ElementPlusIconsVue)) {
  app.component(key, component)
}
app.use(createPinia())
app.use(router)
app.use(ElementPlus, {locale: zhCn})

app.mount('#app')

```

3). 在 `env.d.ts` 中引入ElementPlus的语言包

declare module ‘element-plus/dist/locale/zh-cn.mjs’

#### 2.3 精简项目

由于基于Vue脚手架创建的项目中，里面携带了很多的多余的Vue组件。 并准备对应的组件存放目录 。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6b1f6b8f7ad94e3cb06ac0cd9a77899d.png)

### 3. 页面布局

#### 3.1 介绍

我们在制作一个页面的时候，一定是先关注整体的页面布局，然后再关注具体的细节处理 。 所以这一小节，我们就先来完成页面的整体布局。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/edc7f6f690e64a43b6b24d3d50c97f3b.png)

我们会看到，整个页面分为这么三个部分：

①. 页头部分

②. 侧边栏

③. 主区域

而要完成这样的页面布局，我们其实是可以借助于 `ElementPlus` 中提供的 `Container布局容器` 来实现：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b4fa3d9ae6114c6aacec02d5ffb2e5bf.png)  
 Container布局容器，用于布局的容器组件，方便快速搭建页面的基本结构：

`<el-container>`：外层容器。 当子元素中包含 `<el-header>` 或 `<el-footer>` 时，全部子元素会垂直上下排列， 否则会水平左右排列。

`<el-header>`：顶栏容器。

`<el-aside>`：侧边栏容器。

`<el-main>`：主要区域容器。

`<el-footer>`：底栏容器。

#### 3.2 整体布局

我们可以参照 `ElementPlus` 的官方网站中的 布局，拷贝其源码，然后对其做一个改造。 具体参照的源码如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f37205a2f74e411292832a3f7e0ff539.png)

1). 在 `src/views` 目录下，再创建一个子目录 `layout` ，在其中新建一个页面，页面命名为：`index.vue`。

2). 在 `index.vue` 中准备好基础的组件结构后，就可以将代码直接复制到 `<template> </template>` 标签中。

```
<script setup lang="ts">

</script>

<template>
   <div class="common-layout">
    <el-container>
      <!-- 顶栏 - header -->
      <el-header>Header</el-header>

      <!-- 左侧菜单 & 主区域 -->
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>

</style>

```

然后，我们先根据页面原型中的布局显示进行调整。 先完成顶栏部分的制作，具体的代码如下：

```
<script setup lang="ts">

</script>

<template>
   <div class="common-layout">
    <el-container>
      <!-- 顶栏 - header -->
      <el-header class="header">
        <span class="title">智能学习辅助系统</span>
        <span class="right_tool">
          <a href=""><el-icon><EditPen /></el-icon> 修改密码 &nbsp;&nbsp;&nbsp;&nbsp;</a>
          <a href=""><el-icon><SwitchButton /></el-icon> 退出登录&nbsp;&nbsp;&nbsp;&nbsp;</a>
        </span>
      </el-header>

      <!-- 左侧菜单 & 主区域 -->
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>
.header {
  background-image: linear-gradient(to right, #e70cc5, #e94dcf, #eb6fd8, #ec8bdf, #eea5e6);
  line-height: 60px;
}

.title {
  color: white;
  font-size: 35px;
  font-family: 楷体;
  
}

.right_tool {
  float: right;
}

a {
  text-decoration: none;
  color: white;
}
</style>

```

最终的顶栏布局效果如下所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7949054092564fba8b1c6d27594e5b9a.png)

#### 3.3 左侧菜单

顶栏布局完毕之后，接下来，我们再来完成左侧菜单栏的制作。 左侧菜单栏的制作，也不需要我们自己实现，其实在 `ElementPlus` 中已经提供了对应的菜单组件，我们可以直接参考【PS: 其实就是复制过来，参考页面原型和需求，将其改造成我们需要的样子就可以了】。

参考代码的出处如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6088361ac19f4994b53406275a40728a.png)

```
<!-- 左侧菜单 -->
<el-aside width="200px" class="aside">
  <el-scrollbar>
    <el-menu router>
      <!-- 首页菜单 -->
      <el-menu-item index="/index">
        <el-icon><Promotion /></el-icon> 首页
      </el-menu-item>
      
      <!-- 班级管理菜单 -->
      <el-sub-menu index="/manage">
        <template #title>
          <el-icon><Menu /></el-icon> 班级学员管理
        </template>
        <el-menu-item index="/clazz">
          <el-icon><HomeFilled /></el-icon>班级管理
        </el-menu-item>
        <el-menu-item index="/stu">
          <el-icon><UserFilled /></el-icon>学员管理
        </el-menu-item>
      </el-sub-menu>
      
      <!-- 系统信息管理 -->
      <el-sub-menu index="/system">
        <template #title>
          <el-icon><Tools /></el-icon>系统信息管理
        </template>
        <el-menu-item index="/dept">
          <el-icon><HelpFilled /></el-icon>部门管理
        </el-menu-item>
        <el-menu-item index="/emp">
          <el-icon><Avatar /></el-icon>员工管理
        </el-menu-item>
      </el-sub-menu>

      <!-- 数据统计管理 -->
      <el-sub-menu index="/report">
        <template #title>
          <el-icon><Histogram /></el-icon>数据统计管理
        </template>
        <el-menu-item index="/empReport">
          <el-icon><InfoFilled /></el-icon>员工信息统计
        </el-menu-item>
        <el-menu-item index="/stuReport">
          <el-icon><Share /></el-icon>学员信息统计
        </el-menu-item>
        <el-menu-item index="/log">
          <el-icon><Document /></el-icon>日志信息统计
        </el-menu-item>
      </el-sub-menu>
    </el-menu>
  </el-scrollbar>
</el-aside>

```

最终，浏览器打开的效果如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/525388800b6348d9b1af092bf8804b69.png)

到目前为止，`layout/index.vue` 中的内容如下：

```
<script setup lang="ts">

</script>

<template>
   <div class="common-layout">
    <el-container>
      <!-- 顶栏 - header -->
      <el-header class="header">
        <span class="title">智能学习辅助系统</span>
        <span class="right_tool">
          <a href=""><el-icon><EditPen /></el-icon> 修改密码 &nbsp;&nbsp;&nbsp;&nbsp;</a>
          <a href=""><el-icon><SwitchButton /></el-icon> 退出登录&nbsp;&nbsp;&nbsp;&nbsp;</a>
        </span>
      </el-header>
      

      <!-- 左侧菜单 & 主区域 -->
      <el-container>
        <!-- 左侧菜单 -->
        <el-aside width="200px" class="aside">
          <el-scrollbar>
            <el-menu router>
              <!-- 首页菜单 -->
              <el-menu-item index="/index">
                <el-icon><Promotion /></el-icon> 首页
              </el-menu-item>
              
              <!-- 班级管理菜单 -->
              <el-sub-menu index="/manage">
                <template #title>
                  <el-icon><Menu /></el-icon> 班级学员管理
                </template>
                <el-menu-item index="/clazz">
                  <el-icon><HomeFilled /></el-icon>班级管理
                </el-menu-item>
                <el-menu-item index="/stu">
                  <el-icon><UserFilled /></el-icon>学员管理
                </el-menu-item>
              </el-sub-menu>
              
              <!-- 系统信息管理 -->
              <el-sub-menu index="/system">
                <template #title>
                  <el-icon><Tools /></el-icon>系统信息管理
                </template>
                <el-menu-item index="/dept">
                  <el-icon><HelpFilled /></el-icon>部门管理
                </el-menu-item>
                <el-menu-item index="/emp">
                  <el-icon><Avatar /></el-icon>员工管理
                </el-menu-item>
              </el-sub-menu>

              <!-- 数据统计管理 -->
              <el-sub-menu index="/report">
                <template #title>
                  <el-icon><Histogram /></el-icon>数据统计管理
                </template>
                <el-menu-item index="/empReport">
                  <el-icon><InfoFilled /></el-icon>员工信息统计
                </el-menu-item>
                <el-menu-item index="/stuReport">
                  <el-icon><Share /></el-icon>学员信息统计
                </el-menu-item>
                <el-menu-item index="/log">
                  <el-icon><Document /></el-icon>日志信息统计
                </el-menu-item>
              </el-sub-menu>

            </el-menu>
          </el-scrollbar>
        </el-aside>


        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>
.header {
  background-image: linear-gradient(to right, #e70cc5, #e94dcf, #eb6fd8, #ec8bdf, #eea5e6);
  line-height: 60px;
}

.title {
  color: white;
  font-size: 35px;
  font-family: 楷体;
  
}

.right_tool {
  float: right;
}

a {
  text-decoration: none;
  color: white;
}

.aside {
  border: 1px solid #ccc;
  height: 690px;
  width: 220px;
}
</style>

```

目前，我们点击左侧的菜单，右侧主区域展示的内容，还不能做到动态变化。 那应该如何做到动态变化呢 ？

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/70d3c0319c114219bc1e8caec26c3e3e.png)  
 那要完成这个功能效果，我们就需要用到Vue生态中的路由 `Vue-Router`。

### 4. Vue Router

#### 4.1 介绍

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/15e39e7ea85c406a9f7749fca67db01b.png)

* Vue Router：Vue的官方路由。 为Vue提供富有表现力、可配置的、方便的路由。
* Vue中的路由，主要定义的是路径与组件之间的对应关系。

比如，我们打开一个网站，点击左侧菜单，地址栏的地址发生变化。 地址栏地址一旦发生变化，在主区域显示对应的页面组件。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a763280c39894b2082642d28f9daa09a.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/498c500f0b7444ada4f4d17dbeb83c0d.png)

VueRouter主要由以下三个部分组成，如下所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e5bd024bbcb842fc87f171847c0194b8.png)

* VueRouter：路由器类，根据路由请求在路由视图中动态渲染选中的组件
* <router-link>：请求链接组件，浏览器会解析成<a>
* <router-view>：动态视图组件，用来渲染展示与路由路径对应的组件

#### 4.2 入门

介绍完了VueRouter之后，接下来，我们就通过一个入门程序，来演示一下VueRouter的使用。

1). 安装 `vue-router` (创建Vue项目时，已经选择)

> npm install vue-router@4

2). 在 `main.ts` 入口文件中进行配置，加入如下配置

```
import router from './router'

//..... 创建完vue的应用实例后,调用app.use
app.use(router)

```

3). 在 src/views 目录下再定义一个文件夹，在文件夹中再创建一个 vue 组件文件

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/60a682e0f7e14c2fb4e2713bdc845ada.png)

4). 定义路由

在 `src/router/index.ts` 中定义路由表信息，在其中主要是定义请求路径与组件之间的对应关系。 完整的文件内容如下：

```
import { createRouter, createWebHistory } from 'vue-router'

const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [
    {
      path: '/',
      name: 'home',
      component: () => import('../views/layout/index.vue')
    },
    {
      path: '/index',
      name: 'index',
      component: () => import('../views/index/index.vue')
    }
  ]
})

export default router

```

5). 在 `App.vue` 根组件中，定义 `<RouterView></RouterView>` 标签

该标签将用于显示，访问的请求路径对应的组件。

```
<script setup lang="ts">

</script>

<template>
  <RouterView></RouterView>
</template>

<style scoped>

</style>

```

6). 测试

浏览器访问请求路径 http://127.0.0.1:8080/index，展示如下页面内容（该页面内容，就是我们在 `index/index.vue` 中定义的页面内容）：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6bf2fbfc427b482dae28b0f8642fa0ab.png)

浏览器访问请求路径 http://127.0.0.1:5173/，展示如下页面内容 （该页面内容，就是我们在 `layout/index.vue` 中定义的页面内容）

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9ac40ed32c5540b0a3593c6117f7c9fa.png)

到此，我们发现，我们请求不同的请求路径，就可以在页面中显示不同的组件。具体的访问流程如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1fb439d0ac944c9da32ca69318072165.png)

#### 4.3 案例

那接下来，我们就要基于 `VueRouter` 来完成点击 左侧菜单，动态切换主展示区域内容的动态效果。

1). 准备案例的空页面 （资料中已经提供，直接复制到项目的 `src/views` 目录中即可）

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ba645f5d21d449739310bf3ac3186c50.png)  
 2). 在 `src/router/index.ts` 中配置路由信息

这里我们用到了Vue中的嵌套路由，具体定义方式，主要是在配置路由信息时，通过`children` 来描述。如你所见，`children` 配置只是另一个路由数组，就像 `routes` 本身一样。因此，你可以根据自己的需要，不断地嵌套视图。

```
import { createRouter, createWebHistory } from 'vue-router'

const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [
    {
      path: '/',
      name: 'home',
      component: () => import('../views/layout/index.vue'),
      redirect: '/index',
      children: [
        {
          path: 'index',
          name: 'index',
          component: () => import('../views/index/index.vue') //首页
        },
        {
          path: 'emp',
          name: 'emp',
          component: () => import('../views/emp/index.vue') //员工管理
        },
        {
          path: 'dept',
          name: 'dept',
          component: () => import('../views/dept/index.vue') //部门管理
        },
        {
          path: 'clazz',
          name: 'clazz',
          component: () => import('../views/clazz/index.vue') //班级管理
        },
        {
          path: 'stu',
          name: 'stu',
          component: () => import('../views/stu/index.vue') //学员管理
        }
      ]
    }
  ]
})

export default router

```

3). 完善左侧菜单栏 `layout/index.vue`，菜单栏关联路由

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ba166c6e8ef249f4868e3d027594874d.png)

菜单关联了路由之后，我们点击对应的菜单，就会根据菜单的唯一标识 `index`，在地址栏中请求访问对应的地址。

4). 在Vue组件中，动态展示与路由对应的组件 。

需要在 `layout/index.vue` 中的 `<el-main></el-main>` 中添加动态路由视图组件 `<RouterView></RouterView>` 。如下：

```
<!-- 主展示区域 -->
<el-main>
	<RouterView></RouterView>
</el-main>

```

最终完整的 `layout/index.vue` 代码如下：

```
<script setup lang="ts">

</script>

<template>
   <div class="common-layout">
    <el-container>
      <!-- 顶栏 - header -->
      <el-header class="header">
        <span class="title">Tlias智能学习辅助系统</span>
        <span class="right_tool">
          <a href=""><el-icon><EditPen /></el-icon> 修改密码 &nbsp;&nbsp;&nbsp;&nbsp;</a>
          <a href=""><el-icon><SwitchButton /></el-icon> 退出登录&nbsp;&nbsp;&nbsp;&nbsp;</a>
        </span>
      </el-header>
      

      <!-- 左侧菜单 & 主区域 -->
      <el-container>
        <!-- 左侧菜单 -->
        <el-aside width="200px" class="aside">
          <el-scrollbar>
            <el-menu router>
              <!-- 首页菜单 -->
              <el-menu-item index="/index">
                <el-icon><Promotion /></el-icon> 首页
              </el-menu-item>
              
              <!-- 班级管理菜单 -->
              <el-sub-menu index="/manage">
                <template #title>
                  <el-icon><Menu /></el-icon> 班级学员管理
                </template>
                <el-menu-item index="/clazz">
                  <el-icon><HomeFilled /></el-icon>班级管理
                </el-menu-item>
                <el-menu-item index="/stu">
                  <el-icon><UserFilled /></el-icon>学员管理
                </el-menu-item>
              </el-sub-menu>
              
              <!-- 系统信息管理 -->
              <el-sub-menu index="/system">
                <template #title>
                  <el-icon><Tools /></el-icon>系统信息管理
                </template>
                <el-menu-item index="/dept">
                  <el-icon><HelpFilled /></el-icon>部门管理
                </el-menu-item>
                <el-menu-item index="/emp">
                  <el-icon><Avatar /></el-icon>员工管理
                </el-menu-item>
              </el-sub-menu>

              <!-- 数据统计管理 -->
              <el-sub-menu index="/report">
                <template #title>
                  <el-icon><Histogram /></el-icon>数据统计管理
                </template>
                <el-menu-item index="/empReport">
                  <el-icon><InfoFilled /></el-icon>员工信息统计
                </el-menu-item>
                <el-menu-item index="/stuReport">
                  <el-icon><Share /></el-icon>学员信息统计
                </el-menu-item>
                <el-menu-item index="/log">
                  <el-icon><Document /></el-icon>日志信息统计
                </el-menu-item>
              </el-sub-menu>
			
            </el-menu>
          </el-scrollbar>
        </el-aside>

        <!-- 主展示区域 -->
        <el-main>
          <RouterView></RouterView>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>
.header {
  background-image: linear-gradient(to right, #e70cc5, #e94dcf, #eb6fd8, #ec8bdf, #eea5e6);
  line-height: 60px;
}

.title {
  color: white;
  font-size: 35px;
  font-family: 楷体;
  
}

.right_tool {
  float: right;
}

a {
  text-decoration: none;
  color: white;
}

.aside {
  border: 1px solid #ccc;
  height: 690px;
  width: 220px;
}
</style>

```

5). 测试

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b686f4a6146f43aebbe9833958cb3762.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8473e366985f4af9b9f815e242b25eaf.png)

#### 4.4 首页制作

其实首页，我们只需要展示一张图片即可。 直接在 `index/index.vue` 中引入一张图片即可，具体代码如下：

```
<script setup lang="ts">

</script>

<template>
    <img src="@/assets/index.png">
</template>

<style scoped>

</style>

```

最终效果如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/169eec76a6134418b482fe7c59dda031.png)

### 5. 部门管理

部门管理的页面内容，写在 `src/views/dept/index.vue` 中。

#### 5.1部门列表

##### 5.1.1. 基本布局

首先，根据页面原型、需求说明、接口文档，先完成页面的基本布局 。 可以参考 `ElementPlus` 中的组件，拷贝过来适当做一个改造。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ecc2c6f4891448639761119ebea2fc0c.png)  
 部门管理组件 `src/views/dept/index.vue` 具体的页面布局代码如下：

```
<script setup lang="ts">
import {ref} from 'vue'
import type { DeptModelArray } from '@/api/model/model'

//声明列表展示数据
let tableData = ref<DeptModelArray>([])
</script>

<template>
  <h1>部门管理</h1>
  <el-button type="primary" style="float: right" @click="">+ 新增</el-button>
  <br><br>

  <!-- 部门数据表格 -->
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column type="index" label="序号"  width="80"  align="center"/>
    <el-table-column prop="name" label="部门名称" width="250"  align="center"/>
    <el-table-column prop="updateTime" label="最后操作时间" width="300"  align="center"/>
    <el-table-column label="操作"  align="center">
      <template #default="scope">
        <el-button size="small" type="primary" @click="">修改</el-button>
        <el-button size="small" type="danger"  @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<style scoped>

</style>

```

表格中每一列展示的属性 `prop` 都是根据接口文档来的，接口文档返回什么样的数据，我们就安装对应的数据格式进行解析。

##### 5.1.2 加载数据

根据需求，需要在新增、修改、删除部门之后，加载最新的部门数据。 在打开页面之后，也需要自动加载部门数据。 那接下来，我们就需要基于axios发送异步请求，动态获取数据。

需要在 `src/views/dept/index.vue` 中增加如下代码，在页面加载完成发送异步请求（https://mock.apifox.com/m1/3161925-0-default/depts），动态加载的Axios。

```
<script setup lang="ts">
import {ref, onMounted} from 'vue'
import type { DeptModelArray } from '@/api/model/model'
import axios from 'axios'

//声明列表展示数据
let tableData = ref<DeptModelArray>([])

//动态加载数据-查询部门
const queryAll = async () => {
  const result = await axios.get('https://mock.apifox.com/m1/3161925-0-default/depts')
  tableData.value = result.data.data
}

//钩子函数
onMounted(() => {
  queryAll()
})
</script>

```

添加代码后，最终 `src/views/dept/index.vue` 代码如下：

```
<script setup lang="ts">
import {ref, onMounted} from 'vue'
import type { DeptModelArray } from '@/api/model/model'
import axios from 'axios'

//声明列表展示数据
let tableData = ref<DeptModelArray>([])

//动态加载数据-查询部门
const queryAll = async () => {
  const result = await axios.get('https://mock.apifox.com/m1/3161925-0-default/depts')
  tableData.value = result.data.data
}

//钩子函数
onMounted(() => {
  queryAll()
})
</script>

<template>
  <h1>部门管理</h1>
  <el-button type="primary" style="float: right" @click="">+ 新增</el-button>
  <br><br>

  <!-- 部门数据表格 -->
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column type="index" label="序号"  width="80"  align="center"/>
    <el-table-column prop="name" label="部门名称" width="250"  align="center"/>
    <el-table-column prop="updateTime" label="最后操作时间" width="300"  align="center"/>
    <el-table-column label="操作"  align="center">
      <template #default="scope">
        <el-button size="small" type="primary" @click="">修改</el-button>
        <el-button size="small" type="danger"  @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<style scoped>

</style>

```

代码编写完成之后，打开浏览器进行测试 ，我们可以看到数据可以正常的查询出来，并展示在页面中。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f358388a92a94b0cb605dccc0bbc2891.png)

**思考：直接在Vue组件中，基于axios发送异步请求，存在什么问题？**

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a0dba05c86eb4069af0fee0a62e91dc0.png)  
 我们刚才在完成部门列表查询时，是直接基于axios发送异步请求，直接将接口的请求地址放在组件文件 `.vue` 中。 而如果开发一个大型的项目，组件文件可能会很多很多很多，如果前端开发完毕，进行前后端联调测试了，需要修改请求地址，那么此时，就需要找到每一个 `.vue` 文件，然后挨个修改。 所以上述的代码，虽然实现了动态加载数据的功能。 但是存在以下问题：

* 请求路径难以维护
* 数据解析繁琐

##### 5.1.3 程序优化

1). 为了解决上述问题，我们在前端项目开发时，通常会定义一个请求处理的工具类 - `src/utils/request.ts` 。 在这个工具类中，对axios进行了封装。 具体代码如下：

```
import axios from 'axios'

//创建axios实例对象
const request = axios.create({
  baseURL: '/api',
  timeout: 600000
})

//axios的响应 response 拦截器
request.interceptors.response.use(
  (response) => { //成功回调
    return response.data
  },
  (error) => { //失败回调
    return Promise.reject(error)
  }
)

export default request

```

2). 而与服务端进行异步交互的逻辑，通常会按模块，封装在一个单独的API中，如：`src/api/dept.ts`

```
import request from "@/utils/request"
import type { ResultModel } from "./model/model"

//列表查询
export const queryAllApi = () => request.get<any, ResultModel>('/depts')

```

3). 修改 `src/views/dept/index.vue` 中的代码

现在就不需要每次直接调用axios发送异步请求了，只需要将我们定义的对应模块的API导入进来，就可以直接使用了。

做完上面这三部之后，我们打开浏览器发现，并不能访问到接口数据。原因是因为，目前请求路径不对。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d90e5aecbcc240d2a09d1a934e156fd4.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/288f2bfc87704b0085770e3e31283184.png)

4). 在 `vite.config.ts` 中配置前端请求服务器的信息

在服务器中配置代理proxy的信息，并在配置代理时，执行目标服务器。 以及url路径重写的规则。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c55d35c19bdd477db199d9cb3cf635f9.png)

```
  server: {
    proxy: {
      '/api': {
        target: 'http://localhost:8080',
        secure: false,
        changeOrigin: true,
        rewrite: (path) => path.replace(/^\/api/, ''),
      }
    }
  }

```

添加位置如下所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bab3f0cd90164232815f82e2c4b24d2b.png)

然后，我们就可以启动服务器端的程序，进行测试了（测试时，记得将之前编写的登录校验的过滤器、拦截器、AOP程序全部注释掉）。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/eb24b5656c314f7c8b451d744815a19a.png)

#### 5.2 新增部门

接下来，我们再来完成新增部门的功能实现。

1). 在 `src/views/dept/index.vue` 中完成页面布局，并编写交互逻辑，完成数据绑定。

完整代码如下：

```
<script setup lang="ts">
import {ref, onMounted} from 'vue'
import type { DeptModelArray, DeptModel } from '@/api/model/model'
import {queryAllApi, addApi} from '@/api/dept'
import { ElMessage } from 'element-plus';

//声明列表展示数据
let tableData = ref<DeptModelArray>([])

//动态加载数据-查询部门
const queryAll = async () => {
  const result = await queryAllApi()
  tableData.value = result.data
}

//钩子函数
onMounted(() => {
  queryAll()
})


//新增部门
const dialogFormVisible = ref<boolean>(false) 
const deptForm = ref<DeptModel>({name: ''})
const formTitle = ref<string>('')

//点击新增按钮触发的函数
const add = () => {
  formTitle.value = '新增部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}
}

//点击保存按钮-发送异步请求
const save = async () => {
  const result = await addApi(deptForm.value)
  if(result.code){
    ElMessage.success('操作成功')
  }else{
    ElMessage.error(result.msg)
  }
  dialogFormVisible.value = false
  queryAll()
}

</script>

<template>
  <h1>部门管理</h1>
  <el-button type="primary" style="float: right" @click="add">+ 新增</el-button>
  <br><br>

  <!-- 部门数据表格 -->
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column type="index" label="序号"  width="80"  align="center"/>
    <el-table-column prop="name" label="部门名称" width="250"  align="center"/>
    <el-table-column prop="updateTime" label="最后操作时间" width="300"  align="center"/>
    <el-table-column label="操作"  align="center">
      <template #default="scope">
        <el-button size="small" type="primary" @click="">修改</el-button>
        <el-button size="small" type="danger"  @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>

  <!-- 新增部门 / 修改部门对话框 -->
  <el-dialog v-model="dialogFormVisible" :title="formTitle" width="30%">
    <el-form :model="deptForm">
      <el-form-item label="部门名称" label-width="80px">
        <el-input v-model="deptForm.name" autocomplete="off" />
      </el-form-item>
    </el-form>

    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogFormVisible = false">取消</el-button>
        <el-button type="primary" @click="save">确定</el-button>
      </span>
    </template>
  </el-dialog>

</template>

<style scoped>

</style>

```

2). 在 `src/api/dept.ts` 中增加如下代码

```
//添加部门
export const addApi = (dept:DeptModel) => request.post<any, ResultModel>('/depts', dept)

```

目前 `src/api/dept.ts` 文件中完整代码如下:

```
import request from "@/utils/request"
import type { DeptModel, ResultModel } from "./model/model"

//列表查询
export const queryAllApi = () => request.get<any, ResultModel>('/depts')

//添加部门
export const addApi = (dept:DeptModel) => request.post<any, ResultModel>('/depts', dept)

```

打开浏览器进行测试，效果如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8a81a9829d3347aaa4da7a6c6f113da4.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1cfecd17aaf945558d3eb8063dffd509.png)

#### 5.3 修改部门

对于修改操作，通常会分为两步进行：

1. 查询回显
2. 保存修改

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cd3859e7d0b543c2b66ba9f464ae53d2.png)

交互逻辑：

1. 点击 编辑 按钮，根据ID进行查询，弹出对话框，完成页面回显展示。（查询回显）
2. 点击 确定 按钮，保存修改后的数据，完成数据更新操作。（保存修改）

##### 5.3.1 查询回显

1). 在 `src/api/dept.ts` 中定义根据id查询的请求

```
//根据ID查询
export const queryInfoApi = (id:number) => request.get(`/depts/${id}`)

```

2). 在 `src/views/dept/index.vue` 中添加根据ID查询回显的逻辑

为修改按钮绑定事件 `<template></template>`:

```
<el-button size="small" type="primary" @click="update(scope.row.id)">修改</el-button>

```

在 `<script> </script>` 添加JS逻辑：

```
//修改部门-查询回显
const update = async (id:number) => {
  formTitle.value = '修改部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}

  const result = await queryInfoApi(id)
  deptForm.value = result.data
}

```

到目前为止，完整的 `src/views/dept/index.vue` 代码如下：

```
<script setup lang="ts">
import {ref, onMounted} from 'vue'
import type { DeptModelArray, DeptModel } from '@/api/model/model'
import {queryAllApi, addApi, queryInfoApi} from '@/api/dept'
import { ElMessage } from 'element-plus';

//声明列表展示数据
let tableData = ref<DeptModelArray>([])

//动态加载数据-查询部门
const queryAll = async () => {
  const result = await queryAllApi()
  tableData.value = result.data
}

//钩子函数
onMounted(() => {
  queryAll()
})


//新增部门
const dialogFormVisible = ref<boolean>(false) 
const deptForm = ref<DeptModel>({name: ''})
const formTitle = ref<string>('')

//点击新增按钮触发的函数
const add = () => {
  formTitle.value = '新增部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}
}

//点击保存按钮-发送异步请求
const save = async () => {
  const result = await addApi(deptForm.value)
  if(result.code){
    ElMessage.success('操作成功')
  }else{
    ElMessage.error(result.msg)
  }
  dialogFormVisible.value = false
  queryAll()
}

//修改部门-查询回显
const update = async (id:number) => {
  formTitle.value = '修改部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}

  const result = await queryInfoApi(id)
  deptForm.value = result.data
}

</script>

<template>
  <h1>部门管理</h1>
  <el-button type="primary" style="float: right" @click="add">+ 新增</el-button>
  <br><br>

  <!-- 部门数据表格 -->
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column type="index" label="序号"  width="80"  align="center"/>
    <el-table-column prop="name" label="部门名称" width="250"  align="center"/>
    <el-table-column prop="updateTime" label="最后操作时间" width="300"  align="center"/>
    <el-table-column label="操作"  align="center">
      <template #default="scope">
        <el-button size="small" type="primary" @click="update(scope.row.id)">修改</el-button>
        <el-button size="small" type="danger"  @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>

  <!-- 新增部门 / 修改部门对话框 -->
  <el-dialog v-model="dialogFormVisible" :title="formTitle" width="30%">
    <el-form :model="deptForm">
      <el-form-item label="部门名称" label-width="80px">
        <el-input v-model="deptForm.name" autocomplete="off" />
      </el-form-item>
    </el-form>

    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogFormVisible = false">取消</el-button>
        <el-button type="primary" @click="save">确定</el-button>
      </span>
    </template>
  </el-dialog>

</template>

<style scoped>

</style>

```

##### 5.3.2 保存修改

由于 新增部门 和 修改部门使用的是同一个Dialog对话框，当前点击 “确定” 按钮的时候，有可能执行的是新增操作，也有可能是修改操作。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/717f204f9d0749359655738ef46aa31b.png)

那应该如何辨别到底是新增，还是修改操作呢 ？

其实，我们只需要根据 `deptForm` 对象的id属性值，来判断即可。 如果没有id，则是新增操作 ；如果有id，则是修改操作。

所以，保存修改功能实现如下：

1). 在 `src/api/dept.ts` 中增加如下修改部门的请求

```
//修改部门
export const updateApi = (dept:DeptModel) => request.put<any, ResultModel>('/depts', dept)

```

2). 在 `src/views/dept/index.vue` 中完善(修改) save 函数的逻辑

```
//点击保存按钮-发送异步请求
const save = async () => {
  let result = null;
  if(deptForm.value.id){
    result = await updateApi(deptForm.value) //有id, 执行修改操作
  }else {
    result = await addApi(deptForm.value) //没有id, 执行新增操作
  }

  if(result.code){
    ElMessage.success('操作成功')
  }else{
    ElMessage.error(result.msg)
  }
  dialogFormVisible.value = false
  queryAll()
}

```

#### 5.4 删除部门

1). 在 `src/api/dept.ts` 中增加如下删除部门的请求

```
//删除部门
export const deleteApi = (id:number) => request.delete<any, ResultModel>(`/depts?id=${id}`)

```

2). 在 `src/views/dept/index.vue` 中为什么 删除 按钮绑定事件

```
<el-button size="small" type="danger"  @click="deleteById(scope.row.id)">删除</el-button>

```

3). 在 `src/views/dept/index.vue` 编写根据ID删除数据的函数

```
//删除部门
const deleteById =async (id:number) => {
  //弹出确认框
  ElMessageBox.confirm('您确认删除此部门吗? ', '确认删除').then( async () => {
    let result = await deleteApi(id)
    if(result.code){ //成功
      ElMessage.success('删除成功')
      queryAll()
    }else {
      ElMessage.error(result.msg)
    }
  }).catch(() => {
    ElMessage.info('取消删除')
  })
}

```

打开浏览器做一个测试:

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1942f6c472364106b53c25348702e74b.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e782d2e24cbb4fceaea2d1222aad07ef.png)

#### 5.5 表单校验

目前，我们已经基本完成了部门管理的增删改查操作。 接下来，我们对部门管理的功能进行，最后一块完善工作，增加表单校验。 从页面原型中，我们可以看到，新增部门的时候部门名称，不能为空，而且长度得在2-10之间。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6f8c6cbabb1d44c1a56c0534e7aeb3fd.png)

##### 5.5.1 ElementPlus 参考

Form 组件允许你验证用户的输入是否符合规范，来帮助你找到和纠正错误。`Form` 组件提供了表单验证的功能，只需为 `rules` 属性传入约定的验证规则，并将 `form-Item` 的 `prop` 属性设置为需要验证的特殊键值即可。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b0d797c64bb84cae9f8d5a903e06c6cb.png)

##### 5.5.2 实现

1). 定义表单校验规则

```
//定义表单校验规则
const deptFormRef = ref<FormInstance>()
const rules = ref<FormRules<DeptModel>>({
  name: [
    { required: true, message: '部门名称不能为空', trigger: 'blur' },
    { min: 2, max: 10, message: '部门名称长度在2-10个字之间', trigger: 'blur' },
  ]
})

```

2). 将表单校验规则与表单绑定

为表单 `<el-form>` 绑定 `rules` 属性绑定表单校验规则 。 为每一个表单项，指定 `prop` 属性,设置为需要验证的属性名。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7c574293adbf4922a481303983be42ae.png)

3). 表单提交时，校验表单，校验通过，则允许提交表单。

修改save方法的逻辑，需要加入表单校验的逻辑。

```
//点击保存按钮-发送异步请求
const save = async (form:FormInstance | undefined) => {
  if(!form) return;
  await form.validate(async (valid) => {
    if (valid) {
      let result = null;
      if(deptForm.value.id){
        result = await updateApi(deptForm.value)
      }else {
        result = await addApi(deptForm.value)
      }

      if(result.code){
        ElMessage.success('操作成功')
      }else{
        ElMessage.error(result.msg)
      }
      dialogFormVisible.value = false
      queryAll()
    }
  })
}

```

4). 重置表单校验结果

```
//重置表单校验结果
const resetForm = (formEl: FormInstance | undefined) => {
  if (!formEl) return
  formEl.resetFields()
}

```

然后在点击 “新增” / “修改” 按钮的时候，调用 resetForm 函数，重置表单校验结果。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/dd1175a7dc514876bca98678a00a40f8.png)

最终，部门管理的完整代码如下：

1). `src/api/dept.ts`

```
import request from "@/utils/request"
import type { DeptModel, ResultModel } from "./model/model"

//列表查询
export const queryAllApi = () => request.get<any, ResultModel>('/depts')

//添加部门
export const addApi = (dept:DeptModel) => request.post<any, ResultModel>('/depts', dept)

//根据ID查询
export const queryInfoApi = (id:number) => request.get(`/depts/${id}`)

//修改部门
export const updateApi = (dept:DeptModel) => request.put<any, ResultModel>('/depts', dept)

//删除部门
export const deleteApi = (id:number) => request.delete<any, ResultModel>(`/depts?id=${id}`)


```

2). `src/views/dept/index.vue`

```
<script setup lang="ts">
import {ref, onMounted} from 'vue'
import type { DeptModelArray, DeptModel } from '@/api/model/model'
import {queryAllApi, addApi, queryInfoApi, updateApi, deleteApi} from '@/api/dept'
import { ElMessage, ElMessageBox, type FormInstance, type FormRules } from 'element-plus';

//声明列表展示数据
let tableData = ref<DeptModelArray>([])

//动态加载数据-查询部门
const queryAll = async () => {
  const result = await queryAllApi()
  tableData.value = result.data
}

//钩子函数
onMounted(() => {
  queryAll()
})


//新增部门
const dialogFormVisible = ref<boolean>(false) 
const deptForm = ref<DeptModel>({name: ''})
const formTitle = ref<string>('')

//点击新增按钮触发的函数
const add = () => {
  formTitle.value = '新增部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}
}

//点击保存按钮-发送异步请求
const save = async (form:FormInstance | undefined) => {
  if(!form) return;
  await form.validate(async (valid) => {
    if (valid) {
      let result = null;
      if(deptForm.value.id){
        result = await updateApi(deptForm.value)
      }else {
        result = await addApi(deptForm.value)
      }

      if(result.code){
        ElMessage.success('操作成功')
      }else{
        ElMessage.error(result.msg)
      }
      dialogFormVisible.value = false
      queryAll()
    }
  })
}

//修改部门-查询回显
const update = async (id:number) => {
  formTitle.value = '修改部门'
  dialogFormVisible.value = true
  deptForm.value = {name: ''}

  const result = await queryInfoApi(id)
  deptForm.value = result.data
}

//删除部门
const deleteById =async (id:number) => {
  //弹出确认框
  ElMessageBox.confirm('您确认删除此部门吗? ', '确认删除').then( async () => {
    let result = await deleteApi(id)
    if(result.code){ //成功
      ElMessage.success('删除成功')
      queryAll()
    }else {
      ElMessage.error(result.msg)
    }
  }).catch(() => {
    ElMessage.info('取消删除')
  })
}

//定义表单校验规则
const deptFormRef = ref<FormInstance>()
const rules = ref<FormRules<DeptModel>>({
  name: [
    { required: true, message: '部门名称不能为空', trigger: 'blur' },
    { min: 2, max: 10, message: '部门名称长度在2-10个字之间', trigger: 'blur' },
  ]
})

//重置表单校验结果
const resetForm = (form: FormInstance | undefined) => {
  if (!form) return
  form.resetFields()
}
</script>

<template>
  <h1>部门管理</h1>
  <el-button type="primary" style="float: right" @click="add(); resetForm(deptFormRef);">+ 新增</el-button>
  <br><br>

  <!-- 部门数据表格 -->
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column type="index" label="序号"  width="80"  align="center"/>
    <el-table-column prop="name" label="部门名称" width="250"  align="center"/>
    <el-table-column prop="updateTime" label="最后操作时间" width="300"  align="center"/>
    <el-table-column label="操作"  align="center">
      <template #default="scope">
        <el-button size="small" type="primary" @click="update(scope.row.id); resetForm(deptFormRef);">修改</el-button>
        <el-button size="small" type="danger"  @click="deleteById(scope.row.id)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>

  <!-- 新增部门 / 修改部门对话框 -->
  <el-dialog v-model="dialogFormVisible" :title="formTitle" width="30%">
    <el-form :model="deptForm" :rules="rules" ref="deptFormRef">
      <el-form-item label="部门名称" label-width="80px" prop="name">
        <el-input v-model="deptForm.name" autocomplete="off" />
      </el-form-item>
    </el-form>

    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogFormVisible = false; resetForm(deptFormRef);">取消</el-button>
        <el-button type="primary" @click="save(deptFormRef)">确定</el-button>
      </span>
    </template>
  </el-dialog>

</template>

<style scoped>

</style>


```

## 员工管理

### 1. 条件分页查询

#### 1.1 概述

在页面原型中，我们可以看到在查询员工信息列表时，既需要根据条件动态查询，还需要对查询的结果进行分页处理。

#### 1.3 页面布局

##### 1.3.1 搜索栏

搜索栏制作，主要用到ElementPlus中的组件包括：`Button 组件` `Form 组件` 。 具体的布局代码如下：

```
<script setup lang="ts">
import type { SearchEmpModel } from '@/api/model/model';
import {ref, onMounted} from 'vue'

//搜索栏对象声明
const searchEmp = ref<SearchEmpModel>({
  name: '',
  gender: '',
  begin: '',
  end: '',
  date: []
})

</script>

<template>
  <h1>员工管理</h1> <br>
  <!-- 搜索栏 -->
  <el-form :inline="true" :model="searchEmp" class="demo-form-inline">
    <el-form-item label="姓名">
      <el-input v-model="searchEmp.name" placeholder="请输入员工姓名" clearable />
    </el-form-item>
    
    <el-form-item label="性别">
      <el-select v-model="searchEmp.gender" placeholder="请选择" clearable>
        <el-option label="男" value="1" />
        <el-option label="女" value="2" />
      </el-select>
    </el-form-item>

    <el-form-item label="入职时间">
      <el-date-picker v-model="searchEmp.date" type="daterange" range-separator="到" start-placeholder="开始时间" end-placeholder="结束时间"/>
    </el-form-item>

    <el-form-item>
      <el-button type="primary" @click="">查询</el-button>
      <el-button type="default" @click="">重置</el-button>
    </el-form-item>
  </el-form>

  <!-- 按钮 -->
  <el-button type="primary" @click="">+ 新增员工</el-button>
  <el-button type="danger" @click="">- 批量删除</el-button>

  <!-- 表格 -->

  <!-- 分页栏 -->

</template>

<style scoped>

</style>

```

浏览器打开页面，具体效果如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e62e5650035245b888d4920627a54657.png)

我们可以在表单中，输入搜索条件，看看表单绑定的数据值。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1c6e1e7739374651a9f1535d66122f08.png)

我们可以看到，日期时间组件中选择的开始时间和结束时间，数据绑定到了 `date` 属性中，是一个数组，里面两个值，一个开始时间、一个结束时间。 而在执行查询时，从接口文档中，我们可以看出，需要的是开始时间 `begin` 和 结束时间 `end`。

而当我们选择的入职时间范围发生变化，应该实时计算出 开始时间 `begin` 和 结束时间 `end`，那这里可以通过Vue框架中的 `watch侦听` 来解决。

##### 1.3.2 watch侦听对象

\*\*作用：\*\*侦听一个或多个响应式数据源，并在数据源变化时，调用所给的 回调函数。

**语法：**

1). 导入 watch 函数

2). 执行 watch 函数，传入要侦听的响应式数据源（ref对象）和回调函数

**A. 侦听一个响应式对象**

```
//演示watch侦听
const myname = ref<string>('')
watch(myname, (newVal, oldVal)=>{
  console.log(`name的值, newVal: ${newVal}, oldVal: ${oldVal}`);
})

```

**B. 侦听对象的单个属性**

```
//侦听searchEmp对象中的name的变化
watch(() => searchEmp.value.name,  (newVal , oldVal) => {
   console.log(`name的值, newVal: ${newVal}, oldVal: ${oldVal}`);
})

```

**C. 侦听对象的全部属性（深度侦听）**

```
watch(searchEmp, (newVal, oldVal) => {
  console.log(`name的值, newVal: ${newVal.name}, oldVal: ${oldVal.name}`);
}, {deep: true})

```

> watch函数的第三个参数是可选的，常见两个选项：
>
> * deep(boolean)：是否深度侦听，默认浅层侦听。
> * immediate(boolean)：是否在侦听创建时，立即触发回调函数

案例中，入职日期的侦听如下代码如下：

```
//侦听searchEmp的date属性
watch(() => searchEmp.value.date, (newVal, oldVal) => {
  if(newVal.length>0) {
    searchEmp.value.begin = newVal[0]
    searchEmp.value.end = newVal[1]
  }else {
    searchEmp.value.begin = ''
    searchEmp.value.end = ''
  }
})

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/72884406bc024f7582f469973ddb9a62.png)

##### 1.3.3 数据表格

1). 在 `src/views/emp/index.vue` 中的 `<template> </template>` 部分增加如下内容：

```
 <!-- 表格 -->
 <!-- 列表展示 -->
 <el-table :data="tableData" border style="width: 100%" fit @selection-change="handleSelectionChange">
    <el-table-column type="selection" width="55" />
    <el-table-column prop="name" label="姓名" align="center" width="130px" />
    <el-table-column label="性别" align="center" width="100px">
      <template #default="scope">
        {{ scope.row.gender == 1 ? '男' : '女' }}
      </template>
    </el-table-column>
    <el-table-column prop="image" label="头像" align="center">
      <template #default="scope">
        <img :src="scope.row.image" height="40">
      </template>
    </el-table-column>
    <el-table-column prop="deptName" label="所属部门" align="center" />
    <el-table-column prop="job" label="职位" align="center" width="100px">
      <template #default="scope">
        <span v-if="scope.row.job == 1">班主任</span>
        <span v-else-if="scope.row.job == 2">讲师</span>
        <span v-else-if="scope.row.job == 3">学工主管</span>
        <span v-else-if="scope.row.job == 4">教研主管</span>
        <span v-else-if="scope.row.job == 5">咨询师</span>
        <span v-else>其他</span>
      </template>
    </el-table-column>
    <el-table-column prop="entryDate" label="入职时间" align="center" width="130px" />
    <el-table-column prop="updateTime" label="最后修改时间" align="center" />
    <el-table-column label="操作" align="center">
      <template #default="scope">
        <el-button type="primary" size="small" @click="">编辑</el-button>
        <el-button type="danger" size="small" @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
  <br>

  <!-- 分页组件Pagination -->
  <el-pagination
    v-model:current-page="pagination.currentPage"
    v-model:page-size="pagination.pageSize"
    :page-sizes="[5, 10, 20, 50, 100]"
    layout="total, sizes, prev, pager, next, jumper"
    :total="pagination.total"
    @size-change="handleSizeChange"
    @current-change="handleCurrentChange"
  />

```

2). 在 `src/views/emp/index.vue` 中的 `<script> </script>` 部分增加如下内容：

```
//列表展示数据
const tableData = ref<EmpModelArray>([])

//复选框
let selectIds = ref<number[]>([])
const handleSelectionChange = (selection: any[]) => {
  selectIds.value = selection.map(item => item.id)
}

//分页组件
const pagination = ref<PaginationParam>({currentPage: 1, pageSize: 5, total: 0})
//每页展示记录数发生变化时触发
const handleSizeChange = (pageSize: number) => {
  pagination.value.pageSize = pageSize
  queryPage()
}
//当前页码发生变化时触发
const handleCurrentChange = (page: number) => {
  pagination.value.currentPage = page
  queryPage()
}

//分页条件查询
const queryPage = async () => {
  
}

```

#### 1.4 页面交互

1). 为 “查询” 按钮绑定事件，点击查询按钮调用queryPage函数.

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/01260ef5ecb2422294a7e3bc958fb551.png)

```
//分页条件查询
const queryPage = async () => {
  const result = await queryPageApi(
    searchEmp.value.begin,
    searchEmp.value.end,
    searchEmp.value.gender,
    searchEmp.value.name,
    pagination.value.currentPage,
    pagination.value.pageSize
  )

  if(result.code) {
    tableData.value = result.data.rows
    pagination.value.total = result.data.total
  }
}

//钩子函数
onMounted(() => {
  queryPage()
})

```

2). 为 “重置” 按钮绑定事件 , 点击重置按钮, 清空搜索表单, 并重新查询.

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ae2ad41e579841d881544d7fee61ac7c.png)

```
//重置
const reset = () => {
  searchEmp.value = {name:'', begin:'', end:'', date: [], gender: ''}
  queryPage()
}

```

到此，员工列表的动态条件分页查询，就已经完成了。 目前 `src/views/emp/index.vue` 中的完整代码如下

```
<script setup lang="ts">
import type { EmpModelArray, PaginationParam, SearchEmpModel } from '@/api/model/model'
import {ref, onMounted, watch} from 'vue'
import { queryPageApi} from '@/api/emp'

//搜索栏对象声明
const searchEmp = ref<SearchEmpModel>({ name: '', gender: '', begin: '', end: '', date: []})
//列表展示数据
const tableData = ref<EmpModelArray>([])

//复选框
let selectIds = ref<number[]>([])
const handleSelectionChange = (selection: any[]) => {
  selectIds.value = selection.map(item => item.id)
}

//分页组件
const pagination = ref<PaginationParam>({currentPage: 1, pageSize: 5, total: 0})
//每页展示记录数发生变化时触发
const handleSizeChange = (pageSize: number) => {
  pagination.value.pageSize = pageSize
  queryPage()
}

//当前页码发生变化时触发
const handleCurrentChange = (page: number) => {
  pagination.value.currentPage = page
  queryPage()
}

//分页条件查询
const queryPage = async () => {
  const result = await queryPageApi(
    searchEmp.value.begin,
    searchEmp.value.end,
    searchEmp.value.gender,
    searchEmp.value.name,
    pagination.value.currentPage,
    pagination.value.pageSize
  )

  if(result.code) {
    tableData.value = result.data.rows
    pagination.value.total = result.data.total
  }
}

//钩子函数
onMounted(() => {
  queryPage()
})


//重置
const reset = () => {
  searchEmp.value = {name:'', begin:'', end:'', date: [], gender: ''}
  queryPage()
}


//侦听searchEmp的date属性
watch(() => searchEmp.value.date, (newVal, oldVal) => {
  if(newVal.length>0) {
    searchEmp.value.begin = newVal[0]
    searchEmp.value.end = newVal[1]
  }else {
    searchEmp.value.begin = ''
    searchEmp.value.end = ''
  }
})

</script>

<template>
  <h1>员工管理</h1> <br>
  <!-- 搜索栏 -->
  <el-form :inline="true" :model="searchEmp" class="demo-form-inline">
    <el-form-item label="姓名">
      <el-input v-model="searchEmp.name" placeholder="请输入员工姓名" clearable />
    </el-form-item>
    
    <el-form-item label="性别">
      <el-select v-model="searchEmp.gender" placeholder="请选择" clearable>
        <el-option label="男" value="1" />
        <el-option label="女" value="2" />
      </el-select>
    </el-form-item>

    <el-form-item label="入职时间">
      <el-date-picker v-model="searchEmp.date" type="daterange" value-format="YYYY-MM-DD" range-separator="到" start-placeholder="开始时间" end-placeholder="结束时间"/>
    </el-form-item>

    <el-form-item>
      <el-button type="primary" @click="queryPage()">查询</el-button>
      <el-button type="default" @click="reset()">重置</el-button>
    </el-form-item>
  </el-form>

  <!-- 按钮 -->
  <el-button type="primary" @click="">+ 新增员工</el-button>
  <el-button type="danger" @click="">- 批量删除</el-button>
  <br><br>
  

  <!-- 表格 -->
  <!-- 列表展示 -->
  <el-table :data="tableData" border style="width: 100%" fit @selection-change="handleSelectionChange">
    <el-table-column type="selection" width="55" />
    <el-table-column prop="name" label="姓名" align="center" width="130px" />
    <el-table-column label="性别" align="center" width="100px">
      <template #default="scope">
        {{ scope.row.gender == 1 ? '男' : '女' }}
      </template>
    </el-table-column>
    <el-table-column prop="image" label="头像" align="center">
      <template #default="scope">
        <img :src="scope.row.image" height="40">
      </template>
    </el-table-column>
    <el-table-column prop="deptName" label="所属部门" align="center" />
    <el-table-column prop="job" label="职位" align="center" width="100px">
      <template #default="scope">
        <span v-if="scope.row.job == 1">班主任</span>
        <span v-else-if="scope.row.job == 2">讲师</span>
        <span v-else-if="scope.row.job == 3">学工主管</span>
        <span v-else-if="scope.row.job == 4">教研主管</span>
        <span v-else-if="scope.row.job == 5">咨询师</span>
        <span v-else>其他</span>
      </template>
    </el-table-column>
    <el-table-column prop="entryDate" label="入职时间" align="center" width="130px" />
    <el-table-column prop="updateTime" label="最后修改时间" align="center" />
    <el-table-column label="操作" align="center">
      <template #default="scope">
        <el-button type="primary" size="small" @click="">编辑</el-button>
        <el-button type="danger" size="small" @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
  <br>

  <!-- 分页组件Pagination -->
  <el-pagination
    v-model:current-page="pagination.currentPage"
    v-model:page-size="pagination.pageSize"
    :page-sizes="[5, 10, 20, 50, 100]"
    layout="total, sizes, prev, pager, next, jumper"
    :total="pagination.total"
    @size-change="handleSizeChange"
    @current-change="handleCurrentChange"
  />
  
</template>

<style scoped>

</style>

```

最终，打开浏览器效果如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e6a899ad6a2040b1886bdc1e716b143a.png)

### 2. 新增员工

#### 2.1 需求分析

通过页面原型，我们可以看到，新增员工的表单提交的数据，包括员工的基本数据，员工的工作经历数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d2aaac966d874fc3bb669fc5cd86abcb.png)

#### 2.2 页面布局

##### 2.2.1 介绍

我们看到这个表单，每一行放了两个表单项。 而头像这一行，是一个表单项，这里呢，我们可以使用 `ElementPlus` 提供的 `layout` 布局来实现。通过基础的 24 分栏，迅速简便地创建布局。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6f4e882ab6c8461395646ea622acd126.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/aa0ae5241fcc433487d1168eb838209d.png)

##### 2.2.2 基本信息

先来完成员工基本信息表单的制作。 具体的代码如下：

1). `<template> </template>` 中的布局代码如下

```
<!-- 新增员工/修改员工-Dialog -->
  <!-- 新增/修改员工对话框 -->
  <el-dialog v-model="dialogFormVisible" :title="formTitle">
    <el-form :model="emp" >
      <!-- 第一行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="用户名" :label-width="labelWidth" prop="username">
            <el-input v-model="emp.username" />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="姓名" :label-width="labelWidth" prop="name">
            <el-input v-model="emp.name" />
          </el-form-item>
        </el-col>
      </el-row>
      
      <!-- 第二行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="性别" :label-width="labelWidth"  prop="gender">
            <el-select v-model="emp.gender" placeholder="请选择" style="width: 100%;">
              <el-option v-for="gender in genders" :label="gender.name" :value="gender.value" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="手机号" :label-width="labelWidth"  prop="phone">
            <el-input v-model="emp.phone" />
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第三行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="薪资" :label-width="labelWidth"  prop="salary">
            <el-input v-model="emp.salary" />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="入职日期" :label-width="labelWidth">
            <el-date-picker v-model="emp.entryDate" type="date" placeholder="请选择入职日期" value-format="YYYY-MM-DD" style="width: 100%;"/>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第四行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="所属部门" :label-width="labelWidth">
            <el-select v-model="emp.deptId" placeholder="请选择" style="width: 100%;">
              <el-option v-for="dept in depts" :label="dept.name" :value="dept.id" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="职位" :label-width="labelWidth">
            <el-select v-model="emp.job" placeholder="请选择" style="width: 100%;">
              <el-option v-for="job in jobs" :label="job.name" :value="job.value" />
            </el-select>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第五行 -->
      <el-row :gutter="10">
        <el-col :span="24">
          <el-form-item label="头像" label-width="80px">
            <el-upload class="avatar-uploader" 
              action="/api/upload" 
              :show-file-list="false"
              :on-success="handleAvatarSuccess" 
              :before-upload="beforeAvatarUpload">
              <img v-if="emp.image"  :src="emp.image" class="avatar" />
              <el-icon v-else class="avatar-uploader-icon"><Plus /></el-icon>
            </el-upload>
          </el-form-item>
        </el-col>
      </el-row>
    </el-form>

    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogFormVisible = false; ">取消</el-button>
        <el-button type="primary" @click="">保存</el-button>
      </span>
    </template>

  </el-dialog>

```

2). `<script> </script>` 中的代码如下

```
//钩子函数 - 添加调用queryAllDept() 代码
onMounted(() => {
  queryPage()
  queryAllDept()
})

//查询所有部门
const depts = ref<DeptModelArray>([])
const queryAllDept = async () => {
  const result = await queryAllApi()
  if(result.code) {
    depts.value = result.data
  }
}


//----------- 新增 / 修改 ---------------------------
//职位列表数据
const jobs = ref([{ name: '班主任', value: 1 },{ name: '讲师', value: 2 },{ name: '学工主管', value: 3 },{ name: '教研主管', value: 4 },{ name: '咨询师', value: 5 },{ name: '其他', value: 6 }])
//性别列表数据
const genders = ref([{ name: '男', value: 1 }, { name: '女', value: 2 }])

let dialogFormVisible = ref<boolean>(false) //控制新增/修改的对话框的显示与隐藏
let labelWidth = ref<number>(80) //form表单label的宽度
let formTitle = ref<string>('') //表单的标题
let emp = ref<EmpModel>({ //员工对象-表单数据绑定
  username: '',
  password: '',
  name: '',
  gender: '',
  phone: '',
  job: '',
  salary: '',
  image: '',
  entryDate: '',
  deptId: '',
  exprList: []
})


//文件上传
// let imageUrl = ref<string>()
const handleAvatarSuccess: UploadProps['onSuccess'] = (response, uploadFile) => {
   emp.value.image = response.data; 
}

const beforeAvatarUpload: UploadProps['beforeUpload'] = (rawFile) => {
  if (rawFile.type !== 'image/jpeg' && rawFile.type !== 'image/png') {
    ElMessage.error('图片格式不支持!')
    return false
  } else if (rawFile.size / 1024 / 1024 > 10) {
    ElMessage.error('图片大小不能超过 10 MB!')
    return false
  }
  return true
}

//新增员工-打开对话框
const add = () => {
  dialogFormVisible.value = true
  formTitle.value = '新增员工'
}

//清空表单
const clearEmp = () => {
  emp.value = {
    username: '',
    password: '',
    name: '',
    gender: '',
    phone: '',
    job: '',
    salary: '',
    image: '',
    entryDate: '',
    deptId: '',
    exprList: new Array<EmpExprModel>()
  }
}

```

3). `<style> </style>` 的css样式代码如下:

```
  .avatar-uploader .avatar {
    width: 78px;
    height: 78px;
    display: block;
  }
  .avatar-uploader .el-upload:hover {
    border-color: var(--el-color-primary);
  }
  .el-icon.avatar-uploader-icon {
    font-size: 28px;
    color: #8c939d;
    width: 78px;
    height: 78px;
    text-align: center;
    border: 1px dashed #ccc;
    border-radius: 5px;
  }

```

打开浏览器，看到新增员工的表单呈现出来了：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e1c7be5bc1604c57b7c5287991129208.png)

##### 2.2.3 工作经历

###### 2.2.3.1 思路

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c74360133ca24f85a1982e0cbc6609d2.png)

新增员工的基本信息表单已经制作完成了，那接下来，要制作的是员工的工作经历。 员工的过往工作经历可能是多条，点击 “添加员工工作经历” 按钮，如何增加一个条目 ？ 点击每一条后面的删除按钮，需要删除当前条件？

* Vue是基于数据驱动视图展示的。
* “添加” 时，我们可以往数组中添加数据。
* “删除” 时，可以删除数组中的元素。
* 一旦数据发生变化，视图中的展示就会发生变化。

###### 2.2.3.2 实现

1). 在 `<template> </template>` 中定义的表单中，增加如下代码：

```
 <!-- 第六行 -->
      <!-- 第六行 -->
      <el-row :gutter="10">
        <el-col :span="24">
          <el-form-item label="工作经历" :label-width="labelWidth">
            <el-button type="success" size="small" @click="addWorkItem">+ 添加工作经历</el-button>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第七...行 -->
      <el-row :gutter="5" v-for="expr in emp.exprList">
        <el-col :span="10">
          <el-form-item label="时间" size="small" :label-width="labelWidth">
            <el-date-picker v-model="expr.exprDate" type="daterange" range-separator="至" start-placeholder="开始时间" end-placeholder="结束时间" value-format="YYYY-MM-DD"/>
          </el-form-item>
        </el-col>
        
        <el-col :span="6">
          <el-form-item label="公司" size="small">
            <el-input v-model="expr.company" placeholder="公司名称"/>
          </el-form-item>
        </el-col>

        <el-col :span="6">
          <el-form-item label="职位" size="small">
            <el-input v-model="expr.job"  placeholder="职位名称"/>
          </el-form-item>
        </el-col>

        <el-col :span="2">
          <el-form-item size="small">
            <el-button type="danger" @click="delWorkItem(expr)">- 删除</el-button>
          </el-form-item>
        </el-col>
      </el-row>

```

2). 在 `<script> </script>` 中增加如下代码：

```
//动态添加工作经历 .
const addWorkItem = () => {
  emp.value.exprList.push({exprDate: [],begin: '',end: '',company: '',job: ''})
}

//动态删除工作经历 .
const delWorkItem = (expr: EmpExprModel) => {
  if(emp.value.exprList) {
    const index = emp.value.exprList.indexOf(expr)
    if(index != -1){
      emp.value.exprList.splice(index,1)
    }
  }
}

//监听-emp员工对象中的工作经历数据
watch(emp, (newVal, oldVal) => {
  if(emp.value.exprList) {
    emp.value.exprList.forEach(expr => {
      expr.begin = expr.exprDate[0]
      expr.end = expr.exprDate[1]
    })
  }
}, {deep: true})

```

打开浏览器，点击 新增员工，点击 “添加员工工作经历” 测试：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7920d9d34aea4ff99b31b4e7bc95745d.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/308ab2935f934a83b94f4947e316827c.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2cd5dca9650d4c549bbd24e491641479.png)

#### 2.3 页面交互

基本的页面布局，我们完成之后，接下来，就需要完成页面的交互操作。 当点击 “保存” 按钮，需要执行如下操作：

1. 点击保存之后，发送异步请求到服务端，提交数据。
2. 保存完毕之后，如果成功，关闭对话框，重新加载列表数据。
3. 保存完毕之后，如果失败，提示错误信息。

具体操作如下：

1). 为 “保存按钮” 绑定事件

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1192c6a310014c649de76a227ef9a486.png)

2). 在 `<script></script>` 中定义函数

```
//-------------保存员工信息 
const save = async () => {
  //表单校验
  let result = await addApi(emp.value)
  if(result.code) {
    ElMessage.success('操作成功')
    dialogFormVisible.value = false
    queryPage()
  }else {
    ElMessage.error(result.msg)
  }
}


```

#### 2.4 表单校验

结合页面原型及接口文档，梳理校验规则：

| 字段 | 是否必填 | 其他限制 |
| --- | --- | --- |
| 用户名 | 是 | 长度2-20 |
| 姓名 | 是 | 2-10 |
| 性别 | 是 |  |
| 手机号 | 是 | 符合手机号规则，正则 |
| 薪资 | 否 | 全为数字，第一位不为0，正则 |

1). 参照 `Element Plus` 中的Form表单组件，定义校验规则；

```
//表单校验规则
const empFormRef = ref<FormInstance>()
const rules = ref<FormRules<EmpModel>>({
  username: [
    { required: true, message: '用户名为必填项', trigger: 'blur' },
    { min: 2, max: 20, message: '用户名长度为2-20个字', trigger: 'blur' }
  ],
  name: [
    { required: true, message: '姓名为必填项', trigger: 'blur' },
    { min: 2, max: 10, message: '姓名长度为2-10个字', trigger: 'blur' }
  ],
  gender: [{ required: true, message: '性别为必填项', trigger: 'change' }],
  phone: [
    { required: true, message: '手机号为必填项', trigger: 'blur' },
    { pattern: /^1[3-9]\d{9}$/g, message: '请输入合法的手机号', trigger: 'blur' }
  ],
  salary: [
    { pattern: /^[1-9]\d*$/g, message: '请输入合法的数字', trigger: 'blur' }
  ]
})

```

2). 将校验规则与Form表单组件进行属性绑定；

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ccf49ffbcdd041c39932b148b777be77.png)  
 3). 在保存员工时，进行表单校验，校验通过再提交数据；

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5346830bf59f4450b532de0f78c2cd5f.png)

完善 `save` 函数，完善后的代码如下：

```
const save = async (form: FormInstance|undefined) => {
  if(!form) return;
  //表单校验
  form.validate(async (valid) => {
    if(valid) {
      let result = await addApi(emp.value)
      if(result.code) {
        ElMessage.success('操作成功')
        dialogFormVisible.value = false
        queryPage()
      }else {
        ElMessage.error(result.msg)
      } 
    }
  })
}

```

4). 点击取消、新增、修改时，重置表单校验规则；

```
//重置表单
const resetForm = (empForm: FormInstance | undefined) => {
  if (!empForm) return
  empForm.resetFields()
}

```

新增员工时，重置表单校验规则：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0e17199b2dff4535928e17b71ac98aa8.png)  
 点击取消时，重置表单校验规则：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0a30b9d61a8e41a3bae54c5a193be9e3.png)  
 打开浏览器，访问测试：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0be55d09a0e24be699100826a23cb84f.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/67f3070f18784e8aa63b20cf44d6acc5.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9f7f4eadc96b49c99bd7c34a20d1ff97.png)  
 到此呢，关于员工列表的动态条件分页查询。 新增员工的功能，我们都已经实现了，目前 `src/views/emp/index.vue` 文件的代码如下:

```
<script setup lang="ts">
import type { DeptModelArray, EmpExprModel, EmpModel, EmpModelArray, PaginationParam, SearchEmpModel } from '@/api/model/model'
import { ref, onMounted, watch } from 'vue'
import { addApi, queryPageApi } from '@/api/emp'
import { queryAllApi } from '@/api/dept'
import { ElMessage, type FormInstance, type FormRules, type UploadProps } from 'element-plus';

//搜索栏对象声明
const searchEmp = ref<SearchEmpModel>({ name: '', gender: '', begin: '', end: '', date: []})
//列表展示数据
const tableData = ref<EmpModelArray>([])

//复选框
let selectIds = ref<number[]>([])
const handleSelectionChange = (selection: any[]) => {
  selectIds.value = selection.map(item => item.id)
}

//分页组件
const pagination = ref<PaginationParam>({currentPage: 1, pageSize: 5, total: 0})
//每页展示记录数发生变化时触发
const handleSizeChange = (pageSize: number) => {
  pagination.value.pageSize = pageSize
  queryPage()
}
//当前页码发生变化时触发
const handleCurrentChange = (page: number) => {
  pagination.value.currentPage = page
  queryPage()
}

//分页条件查询
const queryPage = async () => {
  const result = await queryPageApi(
    searchEmp.value.begin,
    searchEmp.value.end,
    searchEmp.value.gender,
    searchEmp.value.name,
    pagination.value.currentPage,
    pagination.value.pageSize
  )

  if(result.code) {
    tableData.value = result.data.rows
    pagination.value.total = result.data.total
  }
}

//钩子函数
onMounted(() => {
  queryPage()
  queryAllDept()
})

//查询所有部门
const depts = ref<DeptModelArray>([])
const queryAllDept = async () => {
  const result = await queryAllApi()
  if(result.code) {
    depts.value = result.data
  }
}


//重置
const reset = () => {
  searchEmp.value = {name:'', begin:'', end:'', date: [], gender: ''}
  queryPage()
}


//侦听searchEmp的date属性
watch(() => searchEmp.value.date, (newVal, oldVal) => {
  if(newVal.length>0) {
    searchEmp.value.begin = newVal[0]
    searchEmp.value.end = newVal[1]
  }else {
    searchEmp.value.begin = ''
    searchEmp.value.end = ''
  }
})


//----------- 新增 / 修改 ---------------------------
//职位列表数据
const jobs = ref([{ name: '班主任', value: 1 },{ name: '讲师', value: 2 },{ name: '学工主管', value: 3 },{ name: '教研主管', value: 4 },{ name: '咨询师', value: 5 },{ name: '其他', value: 6 }])
//性别列表数据
const genders = ref([{ name: '男', value: 1 }, { name: '女', value: 2 }])

let dialogFormVisible = ref<boolean>(false) //控制新增/修改的对话框的显示与隐藏
let labelWidth = ref<number>(80) //form表单label的宽度
let formTitle = ref<string>('') //表单的标题
let emp = ref<EmpModel>({ //员工对象-表单数据绑定
  username: '',
  password: '',
  name: '',
  gender: '',
  phone: '',
  job: '',
  salary: '',
  image: '',
  entryDate: '',
  deptId: '',
  exprList: []
})


//文件上传
// let imageUrl = ref<string>()
const handleAvatarSuccess: UploadProps['onSuccess'] = (response, uploadFile) => {
   emp.value.image = response.data; 
}

const beforeAvatarUpload: UploadProps['beforeUpload'] = (rawFile) => {
  if (rawFile.type !== 'image/jpeg' && rawFile.type !== 'image/png') {
    ElMessage.error('图片格式不支持!')
    return false
  } else if (rawFile.size / 1024 / 1024 > 10) {
    ElMessage.error('图片大小不能超过 10 MB!')
    return false
  }
  return true
}

//新增员工-打开对话框
const add = () => {
  dialogFormVisible.value = true
  formTitle.value = '新增员工'
}



//动态添加工作经历 .
const addWorkItem = () => {
  emp.value.exprList.push({exprDate: [],begin: '',end: '',company: '',job: ''})
}

//动态删除工作经历 .
const delWorkItem = (expr: EmpExprModel) => {
  if(emp.value.exprList) {
    const index = emp.value.exprList.indexOf(expr)
    if(index != -1){
      emp.value.exprList.splice(index,1)
    }
  }
}


//-------------保存员工信息 
const save = async (form: FormInstance|undefined) => {
  if(!form) return;
  //表单校验
  form.validate(async (valid) => {
    if(valid) {
      let result = await addApi(emp.value)
      if(result.code) {
        ElMessage.success('操作成功')
        dialogFormVisible.value = false
        queryPage()
      }else {
        ElMessage.error(result.msg)
      } 
    }
  })
}

//表单校验规则
const empFormRef = ref<FormInstance>()
const rules = ref<FormRules<EmpModel>>({
  username: [
    { required: true, message: '用户名为必填项', trigger: 'blur' },
    { min: 2, max: 20, message: '用户名长度为2-20个字', trigger: 'blur' }
  ],
  name: [
    { required: true, message: '姓名为必填项', trigger: 'blur' },
    { min: 2, max: 10, message: '姓名长度为2-10个字', trigger: 'blur' }
  ],
  gender: [{ required: true, message: '性别为必填项', trigger: 'change' }],
  phone: [
    { required: true, message: '手机号为必填项', trigger: 'blur' },
    { pattern: /^1[3-9]\d{9}$/g, message: '请输入合法的手机号', trigger: 'blur' }
  ],
  salary: [
    { pattern: /^[1-9]\d*$/g, message: '请输入合法的数字', trigger: 'blur' }
  ]
})

//重置表单
const resetForm = (empForm: FormInstance | undefined) => {
  if (!empForm) return
  empForm.resetFields()
}

//清空表单
const clearEmp = () => {
  emp.value = {
    username: '',
    password: '',
    name: '',
    gender: '',
    phone: '',
    job: '',
    salary: '',
    image: '',
    entryDate: '',
    deptId: '',
    exprList: new Array<EmpExprModel>()
  }
}
</script>

<template>
  <h1>员工管理</h1> <br>
  <!-- 搜索栏 -->
  <el-form :inline="true" :model="searchEmp" class="demo-form-inline">
    <el-form-item label="姓名">
      <el-input v-model="searchEmp.name" placeholder="请输入员工姓名" clearable />
    </el-form-item>
    
    <el-form-item label="性别">
      <el-select v-model="searchEmp.gender" placeholder="请选择" clearable>
        <el-option label="男" value="1" />
        <el-option label="女" value="2" />
      </el-select>
    </el-form-item>

    <el-form-item label="入职时间">
      <el-date-picker v-model="searchEmp.date" type="daterange" value-format="YYYY-MM-DD" range-separator="到" start-placeholder="开始时间" end-placeholder="结束时间"/>
    </el-form-item>

    <el-form-item>
      <el-button type="primary" @click="queryPage()">查询</el-button>
      <el-button type="default" @click="reset()">重置</el-button>
    </el-form-item>
  </el-form>

  <!-- 按钮 -->
  <el-button type="primary" @click="add(); resetForm(empFormRef); clearEmp()">+ 新增员工</el-button>
  <el-button type="danger" @click="">- 批量删除</el-button>
  <br><br>
  


  <!-- 表格 -->
  <!-- 列表展示 -->
  <el-table :data="tableData" border style="width: 100%" fit @selection-change="handleSelectionChange">
    <el-table-column type="selection" width="55" />
    <el-table-column prop="name" label="姓名" align="center" width="130px" />
    <el-table-column label="性别" align="center" width="100px">
      <template #default="scope">
        {{ scope.row.gender == 1 ? '男' : '女' }}
      </template>
    </el-table-column>
    <el-table-column prop="image" label="头像" align="center">
      <template #default="scope">
        <img :src="scope.row.image" height="40">
      </template>
    </el-table-column>
    <el-table-column prop="deptName" label="所属部门" align="center" />
    <el-table-column prop="job" label="职位" align="center" width="100px">
      <template #default="scope">
        <span v-if="scope.row.job == 1">班主任</span>
        <span v-else-if="scope.row.job == 2">讲师</span>
        <span v-else-if="scope.row.job == 3">学工主管</span>
        <span v-else-if="scope.row.job == 4">教研主管</span>
        <span v-else-if="scope.row.job == 5">咨询师</span>
        <span v-else>其他</span>
      </template>
    </el-table-column>
    <el-table-column prop="entryDate" label="入职时间" align="center" width="130px" />
    <el-table-column prop="updateTime" label="最后修改时间" align="center" />
    <el-table-column label="操作" align="center">
      <template #default="scope">
        <el-button type="primary" size="small" @click="">编辑</el-button>
        <el-button type="danger" size="small" @click="">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
  <br>

  <!-- 分页组件Pagination -->
  <el-pagination
    v-model:current-page="pagination.currentPage"
    v-model:page-size="pagination.pageSize"
    :page-sizes="[5, 10, 20, 50, 100]"
    layout="total, sizes, prev, pager, next, jumper"
    :total="pagination.total"
    @size-change="handleSizeChange"
    @current-change="handleCurrentChange"
  />
  

  <!-- 新增员工/修改员工-Dialog -->
  <!-- 新增/修改员工对话框 -->
  <el-dialog v-model="dialogFormVisible" :title="formTitle">
    <el-form :model="emp" ref="empFormRef" :rules="rules">
      <!-- 第一行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="用户名" :label-width="labelWidth" prop="username">
            <el-input v-model="emp.username" />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="姓名" :label-width="labelWidth" prop="name">
            <el-input v-model="emp.name" />
          </el-form-item>
        </el-col>
      </el-row>
      
      <!-- 第二行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="性别" :label-width="labelWidth"  prop="gender">
            <el-select v-model="emp.gender" placeholder="请选择" style="width: 100%;">
              <el-option v-for="gender in genders" :label="gender.name" :value="gender.value" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="手机号" :label-width="labelWidth"  prop="phone">
            <el-input v-model="emp.phone" />
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第三行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="薪资" :label-width="labelWidth"  prop="salary">
            <el-input v-model="emp.salary" />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="入职日期" :label-width="labelWidth">
            <el-date-picker v-model="emp.entryDate" type="date" placeholder="请选择入职日期" value-format="YYYY-MM-DD" style="width: 100%;"/>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第四行 -->
      <el-row>
        <el-col :span="12">
          <el-form-item label="所属部门" :label-width="labelWidth">
            <el-select v-model="emp.deptId" placeholder="请选择" style="width: 100%;">
              <el-option v-for="dept in depts" :label="dept.name" :value="dept.id" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="职位" :label-width="labelWidth">
            <el-select v-model="emp.job" placeholder="请选择" style="width: 100%;">
              <el-option v-for="job in jobs" :label="job.name" :value="job.value" />
            </el-select>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第五行 -->
      <el-row :gutter="10">
        <el-col :span="24">
          <el-form-item label="头像" label-width="80px">
            <el-upload class="avatar-uploader" 
              action="/api/upload" 
              :show-file-list="false"
              :on-success="handleAvatarSuccess" 
              :before-upload="beforeAvatarUpload">
              <img v-if="emp.image"  :src="emp.image" class="avatar" />
              <el-icon v-else class="avatar-uploader-icon"><Plus /></el-icon>
            </el-upload>
          </el-form-item>
        </el-col>
      </el-row>


      <!-- 第六行 -->
      <!-- 第六行 -->
      <el-row :gutter="10">
        <el-col :span="24">
          <el-form-item label="工作经历" :label-width="labelWidth">
            <el-button type="success" size="small" @click="addWorkItem">+ 添加工作经历</el-button>
          </el-form-item>
        </el-col>
      </el-row>

      <!-- 第七...行 -->
      <el-row :gutter="5" v-for="expr in emp.exprList">
        <el-col :span="10">
          <el-form-item label="时间" size="small" :label-width="labelWidth">
            <el-date-picker v-model="expr.exprDate" type="daterange" range-separator="至" start-placeholder="开始时间" end-placeholder="结束时间" value-format="YYYY-MM-DD"/>
          </el-form-item>
        </el-col>
        
        <el-col :span="6">
          <el-form-item label="公司" size="small">
            <el-input v-model="expr.company" placeholder="公司名称"/>
          </el-form-item>
        </el-col>

        <el-col :span="6">
          <el-form-item label="职位" size="small">
            <el-input v-model="expr.job"  placeholder="职位名称"/>
          </el-form-item>
        </el-col>

        <el-col :span="2">
          <el-form-item size="small">
            <el-button type="danger" @click="delWorkItem(expr)">- 删除</el-button>
          </el-form-item>
        </el-col>
      </el-row>

    </el-form>

    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogFormVisible = false; resetForm(empFormRef)">取消</el-button>
        <el-button type="primary" @click="save(empFormRef)">保存</el-button>
      </span>
    </template>

  </el-dialog>

</template>

<style scoped>
  .avatar-uploader .avatar {
    width: 78px;
    height: 78px;
    display: block;
  }
  .avatar-uploader .el-upload:hover {
    border-color: var(--el-color-primary);
  }
  .el-icon.avatar-uploader-icon {
    font-size: 28px;
    color: #8c939d;
    width: 78px;
    height: 78px;
    text-align: center;
    border: 1px dashed #ccc;
    border-radius: 5px;
  }
</style>

```

## 后端接口开发

## 部门列表查询

### 3.1 功能实现

#### 3.1.1 需求

查询数据库表中的所有部门数据，展示在页面上。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/27be62dfc58a4dbc8807f361defc967d.png)

#### 3.1.2 实现

1. 准备数据库表 dept 及 实体类 Dept

```
-- 部门管理
create table dept(
    id int unsigned primary key auto_increment comment '主键ID',
    name varchar(10) not null unique comment '部门名称',
    create_time datetime  comment '创建时间',
    update_time datetime  comment '修改时间'
) comment '部门表';

INSERT INTO `dept` VALUES (1,'学工部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
						(2,'教研部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
						(3,'咨询部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
						(4,'就业部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
						(5,'人事部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
						(6,'行政部','2023-09-27 14:00:00','2023-09-27 14:00:00'),
						(7,'综合部','2023-09-25 14:44:19','2023-09-25 14:44:19');

```

```
import lombok.AllArgsConstructor;
import lombok.Data;
import lombok.NoArgsConstructor;
import java.time.LocalDateTime;

@Data
@NoArgsConstructor
@AllArgsConstructor
public class Dept {
    private Integer id;
    private String name;
    private LocalDateTime createTime;
    private LocalDateTime updateTime;
}


```

在项目中引入Mybatis的起步依赖，mysql的驱动包

```
<dependency>
    <groupId>org.mybatis.spring.boot</groupId>
    <artifactId>mybatis-spring-boot-starter</artifactId>
    <version>3.0.3</version>
</dependency>

<dependency>
    <groupId>com.mysql</groupId>
    <artifactId>mysql-connector-j</artifactId>
    <scope>runtime</scope>
</dependency>

```

在项目的application.properties 中引入Mybatis的配置信息 (数据库连接、日志输出)

```
#数据库连接信息
spring.datasource.url=jdbc:mysql://localhost:3306/web01
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=root
spring.datasource.password=123456

#mybatis 日志
mybatis.configuration.log-impl=org.apache.ibatis.logging.stdout.StdOutImpl

```

定义mapper包，并且定义DeptMapper接口，并声明接口方法。

```
import com.itheima.pojo.Dept;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Select;
import java.util.List;

@Mapper
public interface DeptMapper {

    @Select("select * from dept")
    public List<Dept> findAll();

}

```

改造之前编写的dao、service的代码，在service实现中注入mapper接口

* dao层的代码不需要了（备份之后，可以删除）
* service层的代码，需要注入Mapper接口，调用mapper接口方法查询数据库中的数据

```
@Service
public class DeptServiceImpl implements DeptService {
   
    @Autowired
    private DeptMapper deptMapper;

    @Override
    public List<Dept> queryDeptList() {
        return deptMapper.findAll();
    }
}

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/94e9ec68c7ec40b0949e4bfdbef890cd.png)

经过测试，我们发现，创建时间 createTime，修改时间 updateTime 属性并未成功封装。 接下来，我们就需要来处理数据封装问题。

### 3.2 数据封装

我们看到查询返回的结果中大部分字段是有值的，但是createTime，updateTime这两个字段是没有值的，而数据库中是有对应的字段值的，这是为什么呢？

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c6faa37e70b94726b4787288b3e80988.png)

原因如下：

* 实体类属性名和数据库表查询返回的字段名一致，mybatis会自动封装。
* 如果实体类属性名和数据库表查询返回的字段名不一致，不能自动封装。

解决方案：

1. 起别名
2. 结果映射
3. 开启驼峰命名

**1. 起别名**：在SQL语句中，对不一样的列名起别名，别名和实体类属性名一样

```
@Select("select id, name, create_time createTime, update_time updateTime from dept")
public List<Dept> findAll();

```

**2. 手动结果映射**：通过 @Results及@Result 进行手动结果映射

```
@Results({@Result(column = "create_time", property = "createTime"),
          @Result(column = "update_time", property = "updateTime")})
@Select("select id, name, create_time, update_time from dept")
public List<Dept> findAll();

```

`@Results`源代码：

```
@Documented
@Retention(RetentionPolicy.RUNTIME)
@Target({ElementType.METHOD})
public @interface Results {
	String id() default "";
	Result[] value() default {};  //Result类型的数组
}

```

`@Result`源代码：

```
@Documented
@Retention(RetentionPolicy.RUNTIME)
@Target({ElementType.METHOD})
@Repeatable(Results.class)
public @interface Result {
	boolean id() default false;//表示当前列是否为主键（true:是主键）
	String column() default "";//指定表中字段名
	String property() default "";//指定类中属性名
}

```

**3. 开启驼峰命名(推荐)**：如果字段名与属性名符合驼峰命名规则，mybatis会自动通过驼峰命名规则映射



驼峰命名规则： abc\_xyz => abcXyz

* 表中字段名：abc\_xyz
* 类中属性名：abcXyz

```
# 在application.properties中添加：
mybatis.configuration.map-underscore-to-camel-case=tru

```

## 部门管理开发

### 1. 删除部门

#### 1.1 需求分析

删除部门数据。在点击 “删除” 按钮，会根据ID删除部门数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/891dd6e654914da5a2e35737d6349741.png)

了解了需求之后，我们再看看接口文档中，关于删除部门的接口的描述，然后根据接口文档进行服务端接口的开发。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/30d37b762b7047ce94f750350d41efd1.png)

#### 1.3 代码实现

**1). Mapper层**

```
    /**
     * 根据ID删除部门数据
     *
     * # 符号: 占位符，会被 ？替换为预编译的SQL(推荐); 通常用于字段值的替换.
     * $ 符号: 字符串拼接符号，会将参数直接拼接在SQL语句中(不推荐); 如果需要动态设置表名, 字段名时, 必须使用$符号.
     */
    @Delete("delete from dept where id = #{id}")
    void delete(Integer id);

```

> 如果mapper接口方法形参只有一个普通类型的参数，#{…} 里面的属性名可以随便写，如：#{id}、#{value}。

对于 DML 语句来说，执行完毕，也是有返回值的，返回值代表的是增删改操作，影响的记录数，所以可以将执行 DML 语句的方法返回值设置为 Integer。 但是一般开发时，是不需要这个返回值的，所以也可以设置为void。

**2). Service层**

```
@Override
public void delete(Integer id) {
    //Integer deleted = deptMapper.delete(id);
    //System.out.println("删除数据的结果为: " + deleted);
    deptMapper.delete(id);
}

```

**3). Controller层**

```
@DeleteMapping("/depts")
public Result delete(Integer id){
    System.out.println("根据ID删除部门: " + id);
    deptService.delete(id);
    return Result.success();
}

```

代码编写完毕之后，我们就可以启动服务，进行测试了。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f9dff650e5b14157a5a0115c9179108d.png)

### 2. 新增部门

#### 2.1 需求分析

点击 “新增部门” 的按钮之后，弹出新增部门表单，填写部门名称之后，点击确定之后，保存部门数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a51138e8a9b6405e98e0c64154f60eef.png)  
 了解了需求之后，我们再看看接口文档中，关于新增部门的接口的描述，然后根据接口文档进行服务端接口的开发 。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ddfe9ba7768846b0af4bef45da38e6d3.png)

#### 2.3 代码实现

**1). Controller层**

在`DeptController`中增加方法add，具体代码如下：

```
/**
* 添加部门 - json格式参数接收
*/
@Log
@PostMapping
public Result add(@RequestBody Dept dept){
    System.out.println("添加部门: " + dept);
    deptService.add(dept);
    return Result.success();
}

```

**2). Service层**

在`DeptServiceImpl`中增加add方法，完成添加部门的操作，具体代码如下：

```
@Override
public void add(Dept dept) {
    dept.setCreateTime(LocalDateTime.now());
    dept.setUpdateTime(LocalDateTime.now());
    deptMapper.add(dept);
}

```

**3). Mapper层**

在 `DeptMapper` 中增加方法add，完成添加部门的操作具体代码如下：

```
/**
* 添加部门数据 - 传递多个参数时,可以把多个参数封装到一个对象中 , 然后通过 #{属性名} 来获取对象属性
*/
@Insert("insert into dept(name, create_time, update_time) values(#{name}, #{createTime}, #{updateTime})")
void add(Dept dept);

```

如果在mapper接口中，需要传递多个参数，可以把多个参数封装到一个对象中。 在SQL语句中获取参数的时候，`#{...}` 里面写的是对象的属性名【注意是属性名，不是表的字段名】。

代码编写完毕之后，我们就可以启动服务，进行测试了。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b9b74a993b304e6aa22e6087d8c49a3e.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e57c262d165749c991bfa61e2e0f4bac.png)

### 3. 修改部门

对于任何业务的修改功能来说，一般都会分为两步进行：查询回显、修改数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/24e30c4f54de46ff919a8409156b12f1.png)

#### 3.1 查询回显

##### 3.1.1 需求分析

当我们点击 “编辑” 的时候，需要根据ID查询部门数据，然后用于页面回显展示。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/829b35814d1c41f5a812e9259b93bc0d.png)

###### 3.1.2.2 路径参数接收

`/depts/1`，`/depts/2` 这种在url中传递的参数，我们称之为路径参数。 那么如何接收这样的路径参数呢 ？

路径参数：通过请求URL直接传递参数，使用{…}来标识该路径参数，需要使用 @PathVariable 获取路径参数。如下所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b1eb45b9b97e42b9b2f45710d5b697f1.png)

```
/**
* 根据ID查询部门数据
* @return
*/
@GetMapping("/{id}")
public Result getInfo(@PathVariable Integer id){
    System.out.println("根据ID查询部门数据: " + id);
    return Result.success();
}

```

##### 3.1.3 代码实现

**1). Controller层**

在 `DeptController` 中增加 `getInfo` 方法，具体代码如下：

```
/**
* 根据ID查询部门数据
*/
@GetMapping("/{id}")
public Result getInfo(@PathVariable Integer id){
    System.out.println("根据ID查询部门数据: " + id);
    Dept dept = deptService.getInfo(id);
    return Result.success(dept);
}

```

**2). Service层**

在 `DeptServiceImpl` 中增加 `getInfo` 方法，具体代码如下：

```
@Override
public Dept getInfo(Integer id) {
	return deptMapper.getById(id);
}

```

**3). Mapper层**

在 `DeptMapper` 中增加 `getById` 方法，具体代码如下：

```
/**
* 根据ID查询部门数据
*/
@Select("select id, name, create_time, update_time from dept where id = #{id}")
Dept getById(Integer id);

```

代码编写完毕之后，我们就可以启动服务，进行测试了。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e458b6f70cb94da0a9aefa805637586a.png)

#### 3.2 修改数据

##### 3.2.1 需求分析

查询回显回来之后，就可以对部门的信息进行修改了，修改完毕之后，点击确定，此时，就需要根据ID修改部门的数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f53030ef06bb4c87ad3876d6811f786e.png)

##### 3.2.3 代码实现

**1). Controller层**

在 `DeptController` 中增加 `update` 方法，具体代码如下：

```
/**
 * 修改部门数据
 */
@PutMapping
public Result update(@RequestBody Dept dept){
    System.out.println("修改部门数据: " + dept);
    deptService.update(dept);
    return Result.success();
}

```

2). Service层

在 `DeptServiceImpl` 中增加 `update` 方法。 由于是修改操作，每一次修改数据，都需要更新updateTime。所以，具体代码如下：

```
@Override
public void update(Dept dept) {
    dept.setUpdateTime(LocalDateTime.now());
    deptMapper.update(dept);
}

```

**3). Mapper层**

在 `DeptMapper` 中增加 `update` 方法，具体代码如下：

```
/**
 * 根据ID更新部门数据
 */
@Update("update dept set name = #{name}, update_time = #{updateTime} where id = #{id}")
void update(Dept dept);

```

代码编写完毕之后，我们就可以启动服务，进行测试了。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/932bfcc62a77489982781da9f2fac946.png)  
 修改完成之后，我们可以看到最新的数据，如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/84ba6edcc3784e6b9d25ebc6fe604d58.png)

## 多表操作&员工列表查询

### 1. 多表关系

关于单表的操作(单表的设计、单表的增删改查)我们就已经学习完了。接下来我们就要来学习多表的操作，首先来学习多表的设计。

项目开发中，在进行数据库表结构设计时，会根据业务需求及业务模块之间的关系，分析并设计表结构，由于业务之间相互关联，所以各个表结构之间也存在着各种联系，基本上分为三种：

* 一对多(多对一)
* 多对多
* 一对一

#### 2.1 一对多

##### 2.1.1 关系实现

* 场景：部门与员工的关系（一个部门下有多个员工）
* 员工管理页面原型：（前面已完成emp表结构设计）

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7a8f4e71f84241aab9f89da6e3c8a7cd.png)

* 部门管理页面原型：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e86cc2e60daf4d75986dcb48ec13b31e.png)  
 由于一个部门下，会关联多个员工。 而一个员工，是归属于某一个部门的 。那么此时，我们就需要在 `emp` 表中增加一个字段 `dept_id` 来标识这个员工属于哪一个部门，`dept_id` 关联的是 `dept` 的 `id` 。 如下所示：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9327a1c5d1af4cfc84536f1e696a81ad.png)

上述的 `emp` 员工表的 `dept_id` 字段，关联的是 `dept` 部门表的 `id` 。部门表是一的一方，也称为 **父表**，员工表是多的一方，称之为 **子表**。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3c8df5216d724425ad7ea5d5527e3f73.png)  
 那接下来，我们就可以将上述的两张表创建出来。具体SQL语句如下所示：

```
CREATE TABLE dept (
  id int unsigned PRIMARY KEY AUTO_INCREMENT COMMENT 'ID, 主键',
  name varchar(10) NOT NULL UNIQUE COMMENT '部门名称',
  create_time datetime DEFAULT NULL COMMENT '创建时间',
  update_time datetime DEFAULT NULL COMMENT '修改时间'
) COMMENT '部门表';

INSERT INTO dept VALUES (1,'学工部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
					(2,'教研部','2023-09-25 09:47:40','2023-10-09 15:17:04'),
					(3,'咨询部2','2023-09-25 09:47:40','2023-11-30 21:26:24'),
					(4,'就业部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
					(5,'人事部','2023-09-25 09:47:40','2023-09-25 09:47:40'),
					(6,'行政部','2023-11-30 20:56:37','2023-11-30 20:56:37');

create table emp(
    id int unsigned primary key auto_increment comment 'ID,主键',
    username varchar(20) not null unique comment '用户名',
    password varchar(50) default '123456' comment '密码',
    name varchar(10) not null comment '姓名',
    gender tinyint unsigned not null comment '性别, 1:男, 2:女',
    phone char(11) not null unique comment '手机号',
    job tinyint unsigned comment '职位, 1 班主任, 2 讲师 , 3 学工主管, 4 教研主管, 5 咨询师',
    salary int unsigned comment '薪资',
    image varchar(300) comment '头像',
    entry_date date comment '入职日期',
    
    dept_id int unsigned comment '部门ID',  -- 部门ID， 关联部门表的ID字段
    
    create_time datetime comment '创建时间',
    update_time datetime comment '修改时间'
) comment '员工表';


INSERT INTO emp VALUES
(1,'shinaian','123456','施耐庵',1,'13309090001',4,15000,'5.png','2000-01-01',2,'2023-10-20 16:35:33','2023-11-16 16:11:26'),
(2,'songjiang','123456','宋江',1,'13309090002',2,8600,'01.png','2015-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:37'),
(3,'lujunyi','123456','卢俊义',1,'13309090003',2,8900,'01.png','2008-05-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:39'),
(4,'wuyong','123456','吴用',1,'13309090004',2,9200,'01.png','2007-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:41'),
(5,'gongsunsheng','123456','公孙胜',1,'13309090005',2,9500,'01.png','2012-12-05',2,'2023-10-20 16:35:33','2023-10-20 16:35:43'),
(6,'huosanniang','123456','扈三娘',2,'13309090006',3,6500,'01.png','2013-09-05',1,'2023-10-20 16:35:33','2023-10-20 16:35:45'),
(7,'chaijin','123456','柴进',1,'13309090007',1,4700,'01.png','2005-08-01',1,'2023-10-20 16:35:33','2023-10-20 16:35:47'),
(8,'likui','123456','李逵',1,'13309090008',1,4800,'01.png','2014-11-09',1,'2023-10-20 16:35:33','2023-10-20 16:35:49'),
(9,'wusong','123456','武松',1,'13309090009',1,4900,'01.png','2011-03-11',1,'2023-10-20 16:35:33','2023-10-20 16:35:51'),
(10,'linchong','123456','林冲',1,'13309090010',1,5000,'01.png','2013-09-05',1,'2023-10-20 16:35:33','2023-10-20 16:35:53'),
(11,'huyanzhuo','123456','呼延灼',1,'13309090011',2,9700,'01.png','2007-02-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:55'),
(12,'xiaoliguang','123456','小李广',1,'13309090012',2,10000,'01.png','2008-08-18',2,'2023-10-20 16:35:33','2023-10-20 16:35:57'),
(13,'yangzhi','123456','杨志',1,'13309090013',1,5300,'01.png','2012-11-01',1,'2023-10-20 16:35:33','2023-10-20 16:35:59'),
(14,'shijin','123456','史进',1,'13309090014',2,10600,'01.png','2002-08-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:01'),
(15,'sunerniang','123456','孙二娘',2,'13309090015',2,10900,'01.png','2011-05-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:03'),
(16,'luzhishen','123456','鲁智深',1,'13309090016',2,9600,'01.png','2010-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:05'),
(17,'liying','12345678','李应',1,'13309090017',1,5800,'01.png','2015-03-21',1,'2023-10-20 16:35:33','2023-10-20 16:36:07'),
(18,'shiqian','123456','时迁',1,'13309090018',2,10200,'01.png','2015-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:09'),
(19,'gudasao','123456','顾大嫂',2,'13309090019',2,10500,'01.png','2008-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:11'),
(20,'ruanxiaoer','123456','阮小二',1,'13309090020',2,10800,'01.png','2018-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:13'),
(21,'ruanxiaowu','123456','阮小五',1,'13309090021',5,5200,'01.png','2015-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:15'),
(22,'ruanxiaoqi','123456','阮小七',1,'13309090022',5,5500,'01.png','2016-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:17'),
(23,'ruanji','123456','阮籍',1,'13309090023',5,5800,'01.png','2012-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:19'),
(24,'tongwei','123456','童威',1,'13309090024',5,5000,'01.png','2006-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:21'),
(25,'tongmeng','123456','童猛',1,'13309090025',5,4800,'01.png','2002-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:23'),
(26,'yanshun','123456','燕顺',1,'13309090026',5,5400,'01.png','2011-01-01',3,'2023-10-20 16:35:33','2023-11-08 22:12:46'),
(27,'lijun','123456','李俊',1,'13309090027',2,6600,'8.png','2004-01-01',2,'2023-10-20 16:35:33','2023-11-16 17:56:59'),
(28,'lizhong','123456','李忠',1,'13309090028',5,5000,'6.png','2007-01-01',3,'2023-10-20 16:35:33','2023-11-17 16:34:22'),
(30,'liyun','123456','李云',1,'13309090030',NULL,NULL,'01.png','2020-03-01',NULL,'2023-10-20 16:35:33','2023-10-20 16:36:31'),
(36,'linghuchong','123456','令狐冲',1,'18809091212',2,6800,'1.png','2023-10-19',2,'2023-10-20 20:44:54','2023-11-09 09:41:04');

```

**问题：一对多的表关系，在数据库层面该如何实现 ？  
 在数据库表中多的一方，添加字段，来关联一的一方的主键 。**

##### 2.1.2 外键约束

**问题**

表结构创建完毕后，我们看到两张表的数据分别为：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5e95f245a2874de181dba04a34b4668f.png)  
 我们看到，在3号部门下，是关联的有7个员工。 当删除了3号部门后，数据变为：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9e30c256c7264d089d0f7439e39f840a.png)  
 3号部门被删除了，但是依然还有7个员工是属于3号部门的。 此时：就出现数据的不完整、不一致了。

**问题分析**

\*\*现象：\*\*部门数据可以直接删除，然而还有部分员工归属于该部门下，此时就出现了数据的不完整、不一致问题 。

\*\*原因：\*\*目前上述的两张表(员工表、部门表)，在数据库层面，并未建立关联，所以是无法保证数据的一致性和完整性的

**问题解决**

想解决上述的问题呢，我们就可以通过数据库中的 **外键约束** 来解决。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4858b21eabe947898f06f612ed878083.png)  
 外键约束：让两张表的数据建立连接，保证数据的一致性和完整性。

对应的关键字：foreign key

外键约束的语法：

```
-- 创建表时指定
create table 表名(
	字段名    数据类型,
	...
	[constraint]   [外键名称]  foreign  key (外键字段名)   references   主表 (主表列名)	
);


-- 建完表后，添加外键
alter table  表名  add constraint  外键名称  foreign key(外键字段名) references 主表(主表列名);

```

那接下来，我们就为员工表的dept\_id 建立外键约束，来关联部门表的主键。

方式1：通过SQL语句操作

```
-- 修改表： 添加外键约束
alter table tb_emp  add  constraint  fk_dept_id  foreign key (dept_id)  references  tb_dept(id);

```

方式2：图形化界面操作

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/15da790283b64d9c8f1f4baa16d60e42.png)  
 当我们添加外键约束时，我们得保证当前数据库表中的数据是完整的。 所以，我们需要将之前删除掉的数据再添加回来。

当我们添加了外键之后，再删除ID为3的部门，就会发现，此时数据库报错了，不允许删除。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cf9d50d35fdf402398d76423d5133e3e.png)

> 外键约束（foreign key）：保证了数据的完整性和一致性。

**物理外键和逻辑外键**

* 物理外键

  + 概念：使用foreign key定义外键关联另外一张表。
  + 缺点：
    - 影响增、删、改的效率（需要检查外键关系）。
    - 仅用于单节点数据库，不适用与分布式、集群场景。
    - 容易引发数据库的死锁问题，消耗性能。
* 逻辑外键

  + 概念：在业务层逻辑中，解决外键关联。
  + 通过逻辑外键，就可以很方便的解决上述问题。

> \*\*在现在的企业开发中，很少会使用物理外键，都是使用逻辑外键。 甚至在一些数据库开发规范中，会明确指出禁止使用物理外键 foreign key \*\*

#### 2.2 一对一

一对一关系表在实际开发中应用起来比较简单，通常是用来做单表的拆分，也就是将一张大表拆分成两张小表，将大表中的一些基础字段放在一张表当中，将其他的字段放在另外一张表当中，以此来提高数据的操作效率。

一对一的应用场景： 用户表(基本信息+身份信息)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0eb3f5d1a67648219acea91991ec9f85.png)

* 基本信息：用户的ID、姓名、性别、手机号、学历
* 身份信息：民族、生日、身份证号、身份证签发机关，身份证的有效期(开始时间、结束时间)

如果在业务系统当中，对用户的基本信息查询频率特别的高，但是对于用户的身份信息查询频率很低，此时出于提高查询效率的考虑，我就可以将这张大表拆分成两张小表，第一张表存放的是用户的基本信息，而第二张表存放的就是用户的身份信息。他们两者之间一对一的关系，一个用户只能对应一个身份证，而一个身份证也只能关联一个用户。

**那么在数据库层面怎么去体现上述两者之间是一对一的关系呢？  
 其实一对一我们可以看成一种特殊的一对多。一对多我们是怎么设计表关系的？是不是在多的一方添加外键。同样我们也可以通过外键来体现一对一之间的关系，我们只需要在任意一方来添加一个外键就可以了。**

SQL脚本：

```
-- 用户基本信息表
create table tb_user(
    id int unsigned  primary key auto_increment comment 'ID',
    name varchar(10) not null comment '姓名',
    gender tinyint unsigned not null comment '性别, 1 男  2 女',
    phone char(11) comment '手机号',
    degree varchar(10) comment '学历'
) comment '用户基本信息表';
-- 测试数据
insert into tb_user values (1,'白眉鹰王',1,'18812340001','初中'),
                        (2,'青翼蝠王',1,'18812340002','大专'),
                        (3,'金毛狮王',1,'18812340003','初中'),
                        (4,'紫衫龙王',2,'18812340004','硕士');

-- 用户身份信息表
create table tb_user_card(
    id int unsigned  primary key auto_increment comment 'ID',
    nationality varchar(10) not null comment '民族',
    birthday date not null comment '生日',
    idcard char(18) not null comment '身份证号',
    issued varchar(20) not null comment '签发机关',
    expire_begin date not null comment '有效期限-开始',
    expire_end date comment '有效期限-结束',
    user_id int unsigned not null unique comment '用户ID',
    constraint fk_user_id foreign key (user_id) references tb_user(id)
) comment '用户身份信息表';
-- 测试数据
insert into tb_user_card values (1,'汉','1960-11-06','100000100000100001','朝阳区公安局','2000-06-10',null,1),
        (2,'汉','1971-11-06','100000100000100002','静安区公安局','2005-06-10','2025-06-10',2),
        (3,'汉','1963-11-06','100000100000100003','昌平区公安局','2006-06-10',null,3),
        (4,'回','1980-11-06','100000100000100004','海淀区公安局','2008-06-10','2028-06-10',4);

```

#### 2.3 多对多

多对多的关系在开发中属于也比较常见的。比如：学生和老师的关系，一个学生可以有多个授课老师，一个授课老师也可以有多个学生。在比如：学生和课程的关系，一个学生可以选修多门课程，一个课程也可以供多个学生选修。

案例：学生与课程的关系

* 关系：一个学生可以选修多门课程，一门课程也可以供多个学生选择
* 实现关系：建立第三张中间表，中间表至少包含两个外键，分别关联两方主键

SQL脚本：

```
-- 学生表
create table tb_student(
    id int auto_increment primary key comment '主键ID',
    name varchar(10) comment '姓名',
    no varchar(10) comment '学号'
) comment '学生表';
-- 学生表测试数据
insert into tb_student(name, no) 
			values ('黛绮丝', '2000100101'),('谢逊', '2000100102'),('殷天正', '2000100103'),('韦一笑', '2000100104');

-- 课程表
create table tb_course(
   id int auto_increment primary key comment '主键ID',
   name varchar(10) comment '课程名称'
) comment '课程表';
-- 课程表测试数据
insert into tb_course (name) values ('Java'), ('PHP'), ('MySQL') , ('Hadoop');

-- 学生课程表（中间表）
create table tb_student_course(
   id int auto_increment comment '主键' primary key,
   student_id int not null comment '学生ID',
   course_id  int not null comment '课程ID',
   constraint fk_courseid foreign key (course_id) references tb_course (id),
   constraint fk_studentid foreign key (student_id) references tb_student (id)
)comment '学生课程中间表';

-- 学生课程表测试数据
insert into tb_student_course(student_id, course_id) values (1,1),(1,2),(1,3),(2,2),(2,3),(3,4);

```

#### 2.4 案例

下面通过一个综合案例加深对于多表关系的理解，并掌握多表设计的流程。

**需求**

* 根据参考资料中提供的《Talis智能学习辅助系统》页面原型，设计员工管理模块涉及到的表结构。

**步骤**

1. 阅读页面原型及需求文档，分析各个模块涉及到的表结构，及表结构之间的关系。
2. 根据页面原型及需求文档，分析各个表结构中具体的字段及约束。

**分析**

* 页面原型-部门管理

​ ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f978858d0eed4dc986cd913231283563.png)

部门管理涉及到一张部门表，这个前面我们都已经设计过了。 无需再进行设计了。

​

* 页面原型-员工管理  
   ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/10729cf569024df8aeaa19b4221db250.png)  
   ​ 上述在员工列表查询的页面原型，当我们点击 “新增员工” 按钮时，会弹出一个新增员工的表单，表单展示形式如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cfb46da1f1b745eab8c6f33432f4c814.png)

在上述的页面原型中，我们可以看到，每一个员工是归属于某一个部门的，而一个部门下可以有多个员工，所以部门与员工之间的关系是一对多的关系。

​ 从页面员工中，我们可以看到，员工还有工作经历的信息。而每一个员工，是可以添加多个工作经历的。 所以，工作经历我们可以再设计一张表，而员工与员工的工作经历之间的关系，是一对多的关系。

​ 最终，具体的表结构如下：

```
-- 部门表
create table dept (
  id int unsigned PRIMARY KEY AUTO_INCREMENT COMMENT 'ID, 主键',
  name varchar(10) NOT NULL UNIQUE COMMENT '部门名称',
  create_time datetime DEFAULT NULL COMMENT '创建时间',
  update_time datetime DEFAULT NULL COMMENT '修改时间'
) COMMENT '部门表';

-- 员工表
create table emp(
    id int unsigned primary key auto_increment comment 'ID,主键',
    username varchar(20) not null unique comment '用户名',
    password varchar(50) default '123456' comment '密码',
    name varchar(10) not null comment '姓名',
    gender tinyint unsigned not null comment '性别, 1:男, 2:女',
    phone char(11) not null unique comment '手机号',
    job tinyint unsigned comment '职位, 1 班主任, 2 讲师 , 3 学工主管, 4 教研主管, 5 咨询师',
    salary int unsigned comment '薪资',
    image varchar(300) comment '头像',
    entry_date date comment '入职日期',
    dept_id int unsigned comment '部门ID',  -- 关联的是dept部门表的ID
    create_time datetime comment '创建时间',
    update_time datetime comment '修改时间'
) comment '员工表';

-- 员工工作经历表
create table emp_expr(
    id int unsigned primary key auto_increment comment 'ID, 主键',
    emp_id  int unsigned null comment '员工ID', -- 关联的是emp员工表的ID
    begin  date null comment '开始时间',
    end date null comment '结束时间',
    company varchar(50) null comment '公司名称',
    job varchar(50) null comment '职位'
) comment '工作经历';

```

> 注意：在上述的表结构设计中，我们使用的都是逻辑外键。

### 2. 多表查询

#### 2.1 概述

##### 2.1.1 数据准备

SQL脚本：

```
-- 部门管理
create table dept(
    id int unsigned primary key auto_increment comment 'ID, 主键',
    name varchar(10) not null unique comment '部门名称',
    create_time datetime comment '创建时间',
    update_time datetime comment '修改时间'
) comment '部门表' ;

insert into dept (id, name, create_time, update_time) values
        (1,'学工部',now(),now()),
        (2,'教研部',now(),now()),
        (3,'咨询部',now(),now()),
        (4,'就业部',now(),now()),
        (5,'人事部',now(),now()),
	    (6,'行政部',now(),now());

-- 员工管理
create table emp(
    id int unsigned primary key auto_increment comment 'ID,主键',
    username varchar(20) not null unique comment '用户名',
    password varchar(32) not null comment '密码',
    name varchar(10) not null comment '姓名',
    gender tinyint unsigned not null comment '性别, 1:男, 2:女',
    phone char(11) not null unique comment '手机号',
    job tinyint unsigned comment '职位, 1:班主任,2:讲师,3:学工主管,4:教研主管,5:咨询师',
    salary int unsigned comment '薪资',
    image varchar(300) comment '头像',
    entry_date date comment '入职日期',
    dept_id int unsigned COMMENT '关联的部门ID',
    create_time datetime comment '创建时间',
    update_time datetime comment '修改时间'
) comment '员工表';


-- 准备测试数据
INSERT INTO `emp` VALUES 
(1,'shinaian','123456','施耐庵',1,'13309090001',4,15000,'01.png','2000-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:35:35'),
(2,'songjiang','123456','宋江',1,'13309090002',2,8600,'01.png','2015-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:35:37'),
(3,'lujunyi','123456','卢俊义',1,'13309090003',2,8900,'01.png','2008-05-01',2,'2023-10-27 16:35:33','2023-10-27 16:35:39'),
(4,'wuyong','123456','吴用',1,'13309090004',2,9200,'01.png','2007-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:35:41'),(5,'gongsunsheng','123456','公孙胜',1,'13309090005',2,9500,'01.png','2012-12-05',2,'2023-10-27 16:35:33','2023-10-27 16:35:43'),
(6,'huosanniang','123456','扈三娘',2,'13309090006',3,6500,'01.png','2013-09-05',1,'2023-10-27 16:35:33','2023-10-27 16:35:45'),
(7,'chaijin','123456','柴进',1,'13309090007',1,4700,'01.png','2005-08-01',1,'2023-10-27 16:35:33','2023-10-27 16:35:47'),
(8,'likui','123456','李逵',1,'13309090008',1,4800,'01.png','2014-11-09',1,'2023-10-27 16:35:33','2023-10-27 16:35:49'),
(9,'wusong','123456','武松',1,'13309090009',1,4900,'01.png','2011-03-11',1,'2023-10-27 16:35:33','2023-10-27 16:35:51'),
(10,'lichong','123456','林冲',1,'13309090010',1,5000,'01.png','2013-09-05',1,'2023-10-27 16:35:33','2023-10-27 16:35:53'),
(11,'huyanzhuo','123456','呼延灼',1,'13309090011',2,9700,'01.png','2007-02-01',2,'2023-10-27 16:35:33','2023-10-27 16:35:55'),
(12,'xiaoliguang','123456','小李广',1,'13309090012',2,10000,'01.png','2008-08-18',2,'2023-10-27 16:35:33','2023-10-27 16:35:57'),
(13,'yangzhi','123456','杨志',1,'13309090013',1,5300,'01.png','2012-11-01',1,'2023-10-27 16:35:33','2023-10-27 16:35:59'),
(14,'shijin','123456','史进',1,'13309090014',2,10600,'01.png','2002-08-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:01'),
(15,'sunerniang','123456','孙二娘',2,'13309090015',2,10900,'01.png','2011-05-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:03'),
(16,'luzhishen','123456','鲁智深',1,'13309090016',2,9600,'01.png','2010-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:05'),
(17,'liying','12345678','李应',1,'13309090017',1,5800,'01.png','2015-03-21',1,'2023-10-27 16:35:33','2023-10-27 16:36:07'),
(18,'shiqian','123456','时迁',1,'13309090018',2,10200,'01.png','2015-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:09'),
(19,'gudasao','123456','顾大嫂',2,'13309090019',2,10500,'01.png','2008-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:11'),
(20,'ruanxiaoer','123456','阮小二',1,'13309090020',2,10800,'01.png','2018-01-01',2,'2023-10-27 16:35:33','2023-10-27 16:36:13'),
(21,'ruanxiaowu','123456','阮小五',1,'13309090021',5,5200,'01.png','2015-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:15'),
(22,'ruanxiaoqi','123456','阮小七',1,'13309090022',5,5500,'01.png','2016-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:17'),
(23,'ruanji','123456','阮籍',1,'13309090023',5,5800,'01.png','2012-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:19'),
(24,'tongwei','123456','童威',1,'13309090024',5,5000,'01.png','2006-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:21'),
(25,'tongmeng','123456','童猛',1,'13309090025',5,4800,'01.png','2002-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:23'),
(26,'yanshun','123456','燕顺',1,'13309090026',5,5400,'01.png','2011-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:25'),
(27,'lijun','123456','李俊',1,'13309090027',5,6600,'01.png','2004-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:27'),
(28,'lizhong','123456','李忠',1,'13309090028',5,5000,'01.png','2007-01-01',3,'2023-10-27 16:35:33','2023-10-27 16:36:29'),
(29,'songqing','123456','宋清',1,'13309090029',NULL,5100,'01.png','2020-01-01',NULL,'2023-10-27 16:35:33','2023-10-27 16:36:31'),
(30,'liyun','123456','李云',1,'13309090030',NULL,NULL,'01.png','2020-03-01',NULL,'2023-10-27 16:35:33','2023-10-27 16:36:31');

```

##### 2.1.2 介绍

多表查询：查询时从多张表中获取所需数据

> 单表查询的SQL语句：select 字段列表 from 表名;
>
> 那么要执行多表查询，只需要使用逗号分隔多张表即可，如： select 字段列表 from 表1, 表2;

查询用户表和部门表中的数据：

```
select * from  emp , dept;

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8366dc91d5be4c2399b4ac4912056a13.png)

### 3. 员工列表查询

那接下来，我们要来完成的是员工列表的查询功能实现。 具体的需求如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/60484bd7db5f430e8e74de28ee307348.png)  
 在查询员工列表数据时，既需要查询 员工的基本信息，还需要查询员工所属的部门名称，所以这里呢，会涉及到多表查询的操作。

而且，在查询员工列表数据时，既要考虑搜索栏中的查询条件，还要考虑对查询的结果进行分页处理。

那么接下来，我们在实现这个功能时，将会分为三个部分来逐一实现：

* 基本查询
* 分页查询
* 条件分页查询

#### 3.1 环境准备

1). 准备数据库表 `emp(员工表)` `emp_expr(员工工作经历表)`

```
-- 员工表
create table emp(
    id int unsigned primary key auto_increment comment 'ID,主键',
    username varchar(20) not null unique comment '用户名',
    password varchar(50) default '123456' comment '密码',
    name varchar(10) not null comment '姓名',
    gender tinyint unsigned not null comment '性别, 1:男, 2:女',
    phone char(11) not null unique comment '手机号',
    job tinyint unsigned comment '职位, 1 班主任, 2 讲师 , 3 学工主管, 4 教研主管, 5 咨询师',
    salary int unsigned comment '薪资',
    image varchar(300) comment '头像',
    entry_date date comment '入职日期',
    dept_id int unsigned comment '部门ID',
    create_time datetime comment '创建时间',
    update_time datetime comment '修改时间'
) comment '员工表';


INSERT INTO emp VALUES 
(1,'shinaian','123456','施耐庵',1,'13309090001',4,15000,'5.png','2000-01-01',2,'2023-10-20 16:35:33','2023-11-16 16:11:26'),
(2,'songjiang','123456','宋江',1,'13309090002',2,8600,'01.png','2015-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:37'),
(3,'lujunyi','123456','卢俊义',1,'13309090003',2,8900,'01.png','2008-05-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:39'),
(4,'wuyong','123456','吴用',1,'13309090004',2,9200,'01.png','2007-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:41'),
(5,'gongsunsheng','123456','公孙胜',1,'13309090005',2,9500,'01.png','2012-12-05',2,'2023-10-20 16:35:33','2023-10-20 16:35:43'),
(6,'huosanniang','123456','扈三娘',2,'13309090006',3,6500,'01.png','2013-09-05',1,'2023-10-20 16:35:33','2023-10-20 16:35:45'),
(7,'chaijin','123456','柴进',1,'13309090007',1,4700,'01.png','2005-08-01',1,'2023-10-20 16:35:33','2023-10-20 16:35:47'),
(8,'likui','123456','李逵',1,'13309090008',1,4800,'01.png','2014-11-09',1,'2023-10-20 16:35:33','2023-10-20 16:35:49'),
(9,'wusong','123456','武松',1,'13309090009',1,4900,'01.png','2011-03-11',1,'2023-10-20 16:35:33','2023-10-20 16:35:51'),
(10,'linchong','123456','林冲',1,'13309090010',1,5000,'01.png','2013-09-05',1,'2023-10-20 16:35:33','2023-10-20 16:35:53'),
(11,'huyanzhuo','123456','呼延灼',1,'13309090011',2,9700,'01.png','2007-02-01',2,'2023-10-20 16:35:33','2023-10-20 16:35:55'),
(12,'xiaoliguang','123456','小李广',1,'13309090012',2,10000,'01.png','2008-08-18',2,'2023-10-20 16:35:33','2023-10-20 16:35:57'),
(13,'yangzhi','123456','杨志',1,'13309090013',1,5300,'01.png','2012-11-01',1,'2023-10-20 16:35:33','2023-10-20 16:35:59'),
(14,'shijin','123456','史进',1,'13309090014',2,10600,'01.png','2002-08-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:01'),
(15,'sunerniang','123456','孙二娘',2,'13309090015',2,10900,'01.png','2011-05-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:03'),
(16,'luzhishen','123456','鲁智深',1,'13309090016',2,9600,'01.png','2010-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:05'),
(17,'liying','12345678','李应',1,'13309090017',1,5800,'01.png','2015-03-21',1,'2023-10-20 16:35:33','2023-10-20 16:36:07'),
(18,'shiqian','123456','时迁',1,'13309090018',2,10200,'01.png','2015-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:09'),
(19,'gudasao','123456','顾大嫂',2,'13309090019',2,10500,'01.png','2008-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:11'),
(20,'ruanxiaoer','123456','阮小二',1,'13309090020',2,10800,'01.png','2018-01-01',2,'2023-10-20 16:35:33','2023-10-20 16:36:13'),
(21,'ruanxiaowu','123456','阮小五',1,'13309090021',5,5200,'01.png','2015-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:15'),
(22,'ruanxiaoqi','123456','阮小七',1,'13309090022',5,5500,'01.png','2016-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:17'),
(23,'ruanji','123456','阮籍',1,'13309090023',5,5800,'01.png','2012-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:19'),
(24,'tongwei','123456','童威',1,'13309090024',5,5000,'01.png','2006-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:21'),
(25,'tongmeng','123456','童猛',1,'13309090025',5,4800,'01.png','2002-01-01',3,'2023-10-20 16:35:33','2023-10-20 16:36:23'),
(26,'yanshun','123456','燕顺',1,'13309090026',5,5400,'01.png','2011-01-01',3,'2023-10-20 16:35:33','2023-11-08 22:12:46'),
(27,'lijun','123456','李俊',1,'13309090027',2,6600,'8.png','2004-01-01',2,'2023-10-20 16:35:33','2023-11-16 17:56:59'),
(28,'lizhong','123456','李忠',1,'13309090028',5,5000,'6.png','2007-01-01',3,'2023-10-20 16:35:33','2023-11-17 16:34:22'),
(30,'liyun','123456','李云',1,'13309090030',NULL,NULL,'01.png','2020-03-01',NULL,'2023-10-20 16:35:33','2023-10-20 16:36:31'),
(36,'linghuchong','123456','令狐冲',1,'18809091212',2,6800,'1.png','2023-10-19',2,'2023-10-20 20:44:54','2023-11-09 09:41:04');



-- 员工工作经历信息
create table emp_expr(
    id int unsigned primary key auto_increment comment 'ID, 主键',
    emp_id int unsigned comment '员工ID',
    begin date comment '开始时间',
    end  date comment '结束时间',
    company varchar(50) comment '公司名称',
    job varchar(50) comment '职位'
)comment '工作经历';

```

2). 准备与表结构对应的实体类 (资料中提供了, 直接引入到项目中)

```
/**
 * 员工信息
 */
@Data
public class Emp {
    private Integer id; //ID,主键
    private String username; //用户名
    private String password; //密码
    private String name; //姓名
    private Integer gender; //性别, 1:男, 2:女
    private String phone; //手机号
    private Integer job; //职位, 1:班主任,2:讲师,3:学工主管,4:教研主管,5:咨询师
    private Integer salary; //薪资
    private String image; //头像
    private LocalDate entryDate; //入职日期
    private Integer deptId; //关联的部门ID
    private LocalDateTime createTime; //创建时间
    private LocalDateTime updateTime; //修改时间

    //封装部门名称数
    private String deptName; //部门名称
}

```

```
/**
 * 工作经历
 */
@Data
public class EmpExpr {
    private Integer id; //ID
    private Integer empId; //员工ID
    private LocalDate begin; //开始时间
    private LocalDate end; //结束时间
    private String company; //公司名称
    private String job; //职位
}

```

#### 3.2 基本查询

那接下来，我们就先考虑一下要查询所有的员工数据，及其关联的部门名称，这个SQL语句该如何实现 ？

这里，要查询所有的员工，也就意味着，即使员工没有部门，也需要将该员工查询出来 。所以，这里需要用左外连接实现，具体SQL如下：

```
select e.*, d.name from emp as e left join dept as d on e.dept_id = d.id

```

那接下来，我们就定义一个员工管理的mapper接口 `EmpMapper` 并在其中完成员工信息的查询。 具体代码如下：

```
@Mapper
public interface EmpMapper {

    /**
     * 查询所有的员工及其对应的部门名称
     */
    @Select("select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id ")
    public List<Emp> list();

}

```

注意，上述SQL语句中，给 部门名称起了别名 `deptName` ，是因为在接口文档中，要求部门名称给前端返回的数据中，就必须叫 `deptName`。 而这里我们需要将查询返回的每一条记录都封装到Emp对象中，那么就必须保证查询返回的字段名与属性名是一一对应的。

此时，我们就需要在Emp中定义一个属性 `deptName` 用来封装部门名称。 具体如下：

```
@Data
public class Emp {
    private Integer id; //ID,主键
    private String username; //用户名
    private String password; //密码
    private String name; //姓名
    private Integer gender; //性别, 1:男, 2:女
    private String phone; //手机号
    private Integer job; //职位, 1:班主任,2:讲师,3:学工主管,4:教研主管,5:咨询师
    private Integer salary; //薪资
    private String image; //头像
    private LocalDate entryDate; //入职日期
    private Integer deptId; //关联的部门ID
    private LocalDateTime createTime; //创建时间
    private LocalDateTime updateTime; //修改时间

    //封装部门名称数
    private String deptName; //部门名称
}

```

#### 3.3 分页查询

##### 3.3.1 原始分页

###### 3.3.1.1 需求分析

上述我们在Mapper接口中定义了接口方法，完成了查询所有员工及其部门名称的功能，是将数据库中所有的数据查询出来了。 试想如果数据库中的数据有很多(假设有几千几万条)的时候，将数据全部展示出来肯定不现实，那如何解决这个问题呢？

使用分页解决这个问题。每次只展示一页的数据，比如：一页展示10条数据，如果还想看其他的数据，可以通过点击页码进行查询。

而在员工管理的需求中，就要求我们进行分页查询，展示出对应的数据。 具体的页面原型如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2b9b0f0171d6418d8b901d0cc6703967.png)  
 我们继续基于页面原型，继续分析，得出以下结论：

1. 前端在请求服务端时，传递的参数
   * 当前页码 page
   * 每页显示条数 pageSize
2. 后端需要响应什么数据给前端
   * 所查询到的数据列表（存储到List 集合中）
   * 总记录数  
      ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1fb5c26b6f2b49c0bab8e89d50a3f160.png)  
      后台给前端返回的数据包含：List集合(数据列表)、total(总记录数)

而这两部分我们通常封装到PageBean对象中，并将该对象转换为json格式的数据响应回给浏览器。

```
@Data
@NoArgsConstructor
@AllArgsConstructor
public class PageBean {
	private Long total; //总记录数
	private List rows; //当前页数据列表
}

```

###### 3.3.1.2 接口文档

**员工列表查询**

* 基本信息

请求路径：/emps

请求方式：GET

接口描述：该接口用于员工列表数据的条件分页查询

###### 3.3.1.4 代码实现

通过查看接口文档：员工列表查询

> 请求路径：/emps
>
> 请求方式：GET
>
> 请求参数：跟随在请求路径后的参数字符串。 例：/emps?page=1&pageSize=10
>
> 响应数据：json格式

**1). EmpController**

```
@Slf4j
@RequestMapping("/emps")
@RestController
public class EmpController {

    @Autowired
    private EmpService empService;

    @GetMapping
    public Result page(@RequestParam(defaultValue = "1") Integer page ,
                       @RequestParam(defaultValue = "10") Integer pageSize){
        log.info("查询员工信息, page={}, pageSize={}", page, pageSize);
        PageBean pageBean = empService.page(page, pageSize);
        return Result.success(pageBean);
    }

}

```

> @RequestParam(defaultValue=“默认值”) //设置请求参数默认值

**2). EmpService**

```
public interface EmpService {
    /**
     * 分页查询
     * @param page 页码
     * @param pageSize 每页记录数
     */
    PageBean page(Integer page, Integer pageSize);
}

```

**3). EmpServiceImpl**

```
@Service
public class EmpServiceImpl implements EmpService {

    @Autowired
    private EmpMapper empMapper;

    @Override
    public PageBean page(Integer page, Integer pageSize) {
        //1. 获取总记录数
        Long total = empMapper.count();

        //2. 获取结果列表
        Integer start = (page - 1) * pageSize;
        List<Emp> empList = empMapper.list(start, pageSize);

        //3. 封装结果
        return new PageBean(total, empList);
    }
}

```

**4). EmpMapper**

```
@Mapper
public interface EmpMapper {

    /**
     * 查询总记录数
     */
    @Select("select count(*) from emp e left join dept d on e.dept_id = d.id ")
    public Long count();

    /**
     * 查询所有的员工及其对应的部门名称
     */
    @Select("select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id limit #{start}, #{pageSize}")
    public List<Emp> list(Integer start , Integer pageSize);

}

```

###### 3.3.1.6 前后端联调

打开浏览器，测试后端功能接口：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5a24b99f8027482797eda0c00e2dc142.png)

##### 3.3.2 分页插件

###### 3.3.2.1 介绍

前面我们已经完了基础的分页查询，大家会发现：分页查询功能编写起来比较繁琐。 而分页查询的功能是非常常见的，我们查询员工信息需要分页查询，将来在做其他项目时，查询用户信息、订单信息、商品信息等等都是需要进行分页查询的。

而分页查询的思路、步骤是比较固定的。 在Mapper接口中定义两个方法执行两条不同的SQL语句：

1. 查询总记录数
2. 指定页码的数据列表

在Service当中，调用Mapper接口的两个方法，分别获取：总记录数、查询结果列表，然后在将获取的数据结果封装到PageBean对象中。

大家思考下：在未来开发其他项目，只要涉及到分页查询功能(例：订单、用户、支付、商品)，都必须按照以上操作完成功能开发

结论：原始方式的分页查询，存在着"步骤固定"、"代码频繁"的问题

解决方案：可以使用一些现成的分页插件完成。对于Mybatis来讲现在最主流的就是**PageHelper**。

> PageHelper是第三方提供的Mybatis框架中的一款功能强大、方便易用的分页插件，支持任何形式的单标、多表的分页查询。
>
> 官网：https://pagehelper.github.io/

那接下来，我们可以对比一下，使用PageHelper分页插件进行分页 与 原始方式进行分页代码实现的上的差别。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4b7c1a56284e4993941bee1e10f84e40.png)

* Mapper接口层：
  + 原始的分页查询功能中，我们需要在Mapper接口中定义两条SQL语句。
  + PageHelper实现分页查询之后，只需要编写一条SQL语句，而且不需要考虑分页操作，就是一条正常的查询语句。
* Service层：
  + 需要根据页码、每页展示记录数，手动的计算起始索引。
  + 无需手动计算起始索引，直接告诉PageHelper需要查询那一页的数据，每页展示多少条记录即可。

###### 3.3.2.2 代码实现

当使用了PageHelper分页插件进行分页，就无需再Mapper中进行手动分页了。 在Mapper中我们只需要进行正常的列表查询即可。在Service层中，调用Mapper的方法之前设置分页参数，在调用Mapper方法执行查询之后，解析分页结果，并将结果封装到PageBean对象中返回。

1、在pom.xml引入依赖

```
<!--分页插件PageHelper-->
<dependency>
    <groupId>com.github.pagehelper</groupId>
    <artifactId>pagehelper-spring-boot-starter</artifactId>
    <version>1.4.7</version>
</dependency>

```

2、EmpMapper

```
/**
 * 查询所有的员工及其对应的部门名称
 */
@Select("select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id")
public List<Emp> list();

```

3、EmpServiceImpl

```
@Override
public PageBean page(Integer page, Integer pageSize) {
    //1. 设置分页参数
    PageHelper.startPage(page,pageSize);

    //2. 执行查询
    List<Emp> empList = empMapper.list();
    Page<Emp> p = (Page<Emp>) empList;

    //3. 封装结果
    return new PageBean(p.getTotal(), p.getResult());
}

```

#### 3.4 分页查询(带条件)

完了分页查询后，下面我们需要在分页查询的基础上，添加条件。

##### 3.4.1 需求

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/63eac4260ed4440d858aa12a08aecee2.png)  
 通过员工管理的页面原型我们可以看到，员工列表页面的查询，不仅仅需要考虑分页，还需要考虑查询条件。 分页查询我们已经实现了，接下来，我们需要考虑在分页查询的基础上，再加上查询条件。

我们看到页面原型及需求中描述，搜索栏的搜索条件有三个，分别是：

* 姓名：模糊匹配
* 性别：精确匹配
* 入职日期：范围匹配

```
select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id
where 
  e.name like concat('%','张','%')   -- 条件1：根据姓名模糊匹配
  and e.gender = 1                   -- 条件2：根据性别精确匹配
  and e.entry_date = between '2000-01-01' and '2010-01-01'  -- 条件3：根据入职日期范围匹配
order by update_time desc;

```

而且上述的三个条件，都是可以传递，也可以不传递的，也就是动态的。

1). 如果用户仅输入了姓名，则SQL为：

```
select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id where e.name like ? 

```

2). 如果用户仅选择了性别，则SQL为：

```
select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id where e.gender = ?

```

3). 如果用户输入了姓名 和 性别 , 则SQL为：

```
select e.*, d.name deptName from emp as e left join dept as d on e.dept_id = d.id where e.name like ? and e.gender = ?

```

我们需要使用前面学习的Mybatis中的动态SQL 。

###### 3.4.3.1 Controller

**方式一：在Controller方法中通过多个方法形参，依次接收这几个参数**

```
@Slf4j
@RestController
@RequestMapping("/emps")
public class EmpController {

    @Autowired
    private EmpService empService;

    @GetMapping
    public Result page(@RequestParam(defaultValue = "1") Integer page,
                       @RequestParam(defaultValue = "2") Integer pageSize,
                       String name, Integer gender,
                       @DateTimeFormat(pattern = "yyyy-MM-dd") LocalDate begin,
                       @DateTimeFormat(pattern = "yyyy-MM-dd") LocalDate end) {
        log.info("查询请求参数： {}, {}, {}, {}, {}, {}", page, pageSize, name, gender, begin, end);
        PageBean pageBean = null;  //empService.page(page, pageSize);
        return Result.success(pageBean);
    }
}

```

> 场景：如果参数个数比较少，建议直接接收即可。 如果参数个数比较多，这种接收方式不便于维护管理。

**方式二：在Controller方法中通过实体对象封装多个参数。（实体属性与请求参数名保持一致）**

1). 定义实体类

```
@Data
public class EmpQueryParam {

    private Integer page = 1; //页码
    private Integer pageSize = 10; //每页展示记录数
    private String name; //姓名
    private Integer gender; //性别
    @DateTimeFormat(pattern = "yyyy-MM-dd")
    private LocalDate begin; //入职开始时间
    @DateTimeFormat(pattern = "yyyy-MM-dd")
    private LocalDate end; //入职结束时间

}

```

2). Controller方法中通过实体类，封装多个参数

```
/**
* 条件分页查询
*/
@GetMapping
public Result page(EmpQueryParam param) {
    log.info("请求参数： {}", param);
    PageBean pageBean = empService.page(param);
    return Result.success(pageBean);
}

```

> 场景：请求参数比较多时，可以将多个参数封装到一个对象中。

###### 3.4.3.2 Service

1). 在EmpService接口中增加如下方法:

```
    /**
     * 分页条件查询
     */
    PageBean page(EmpQueryParam param);

```

2). 在EmpServiceImpl中实现page方法进行分页条件查询

```
    @Override
    public PageBean page(EmpQueryParam param) {
        //1. 设置分页参数
        PageHelper.startPage(param.getPage(), param.getPageSize());

        //2. 执行查询
        List<Emp> empList = empMapper.list(param);

        //3. 解析封装分页结果
        Page<Emp> p = (Page<Emp>) empList;

        return new PageBean(p.getTotal(), p.getResult());
    }

```

###### 3.4.3.3 Mapper

1). 在EmpMapper中增加如下接口方法 (前面实现的分页查询的方法可以注释了)

```
public List<Emp> list(EmpQueryParam param);

```

2). 创建EmpMapper接口对应的映射配置文件 EmpMapper.xml

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.itheima.mapper.EmpMapper">
    
    <!-- 动态条件查询 -->
    <select id="list" resultType="com.itheima.pojo.Emp">
        select e.*, d.name deptName from emp e left join dept d on e.dept_id = d.id
        <where>
            <if test="name != null and name != ''"> e.name like concat('%', #{name}, '%') </if>
            <if test="gender != null"> and e.gender = #{gender} </if>
            <if test="begin != null and end != null"> and entry_date between #{begin} and #{end} </if>
        </where>
        order by e.update_time desc
    </select>

</mapper>

```

> `<where>` 标签的作用：
>
> 1. 自动根据条件判断是否添加 `where` 关键字
> 2. 可以自动去除掉第一个条件前面多余的 `and` 或 `or`

##### 3.4.5 前后端联调

打开浏览器，测试后端功能接口：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/82c6eedaa73647a59925e65b0080ecb4.png)

## 新增员工

前面我们已经实现了员工信息的条件分页查询。 那今天我们要实现的是新增员工的功能实现，页面原型如下：

首先我们先完成"新增员工"的功能开发，而在"新增员工"中，需要添加头像，而头像需要用到"文件上传"技术。 当整个员工管理功能全部开发完成之后，我们再通过配置文件来优化一些内容。

* 新增员工
* 事务管理
* 文件上传
* 配置文件

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/586f806b7d8743878d822cab9824dfe7.png)

### 1. 新增员工

#### 1.1 需求

#### 1.4 功能开发

##### 1.4.1 准备工作

准备的`EmpExprMapper`接口及映射配置文件`EmpExprMapper.xml`，并准备实体类接收前端传递的json格式的请求参数。

#### 1.4 功能开发

##### 1.4.1 准备工作

准备的`EmpExprMapper`接口及映射配置文件`EmpExprMapper.xml`，并准备实体类接收前端传递的json格式的请求参数。

1). EmpExprMapper接口

```
@Mapper
public interface EmpExprMapper {

}

```

2). EmpExprMapper.xml 配置文件

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.itheima.mapper.EmpExprMapper">

</mapper>

```

3). 需要在 `Emp` 员工实体类中增加属性 `exprList` 来封装工作经历数据。 最终完整代码如下：

```
@Data
public class Emp {
    private Integer id; //ID,主键
    private String username; //用户名
    private String password; //密码
    private String name; //姓名
    private Integer gender; //性别, 1:男, 2:女
    private String phone; //手机号
    private Integer job; //职位, 1:班主任,2:讲师,3:学工主管,4:教研主管,5:咨询师
    private Integer salary; //薪资
    private String image; //头像
    private LocalDate entryDate; //入职日期
    private Integer deptId; //关联的部门ID
    private LocalDateTime createTime; //创建时间
    private LocalDateTime updateTime; //修改时间

    //封装部门名称数
    private String deptName; //部门名称

    //封装员工工作经历信息
    private List<EmpExpr> exprList;
}

```

##### 1.4.2 保存员工基本信息

**1). EmpController**

在 `EmpController` 中增加save方法。

```
/**
 * 添加员工
 */
@PostMapping
public Result save(@RequestBody Emp emp){
    log.info("请求参数emp: {}", emp);
    empService.save(emp);
    return Result.success();
}

```

**2). EmpService & EmpServiceImpl**

在 `EmpService` 中增加 save 方法

```
/**
* 添加员工
* @param emp
*/
void save(Emp emp);

```

在 `EmpServiceImpl` 中增加save方法 , 实现接口中的save方法

```
@Override
public void save(Emp emp) {
    //1.补全基础属性
    emp.setCreateTime(LocalDateTime.now());
    emp.setUpdateTime(LocalDateTime.now());
    
    //2.保存员工基本信息
    empMapper.insert(emp);

    //3. 保存员工的工作经历信息 - 批量 (稍后完成)
    
}

```

**3). EmpMapper**

在 `EmpMapper` 中增加insert方法，新增员工的基本信息。

```
/**
* 新增员工数据
*/
@Options(useGeneratedKeys = true, keyProperty = "id")
@Insert("insert into emp(username, name, gender, phone, job, salary, image, entry_date, dept_id, create_time, update_time) " +
"values (#{username},#{name},#{gender},#{phone},#{job},#{salary},#{image},#{entryDate},#{deptId},#{createTime},#{updateTime})")
void insert(Emp emp);

```

主键返回：@Options(useGeneratedKeys = true, keyProperty = “id”)

由于稍后，我们在保存工作经历信息的时候，需要记录是哪位员工的工作经历。 所以，保存完员工信息之后，是需要获取到员工的ID的，那这里就需要通过Mybatis中提供的主键返回功能来获取。

##### 1.4.3 批量保存工作经历

###### 1.4.3.1 分析

一个员工，是可以有多段工作经历的，所以在页面上将来用户录入员工信息时，可以自己根据需要添加多段工作经历。页面原型展示如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/eebc751a388447b2b0eea2ed2d63e9a2.png)  
 那如果员工只有一段工作经历，我们就需要往工作经历表中保存一条记录。 执行的SQL如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/443c352fa970435c98ad937192b99b07.png)  
 如果员工有两段工作经历，我们就需要往工作经历表中保存两条记录。执行的SQL如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d153cde133b64c95aa70c423fc08aceb.png)  
 如果员工有三段工作经历，我们就需要往工作经历表中保存三条记录。执行的SQL如下：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/03d30f077e904753bc7eaf2328dde999.png)  
 所以，这里最终我们需要执行的是批量插入数据的insert语句。

###### 1.4.3.2 实现

**1). EmpServiceImpl**

完善save方法中保存员工信息的逻辑。完整逻辑如下：

```
@Override
public void save(Emp emp) {
	//1.补全基础属性
    emp.setCreateTime(LocalDateTime.now());
    emp.setUpdateTime(LocalDateTime.now());
    //2.保存员工基本信息
    empMapper.insert(emp);

    //3. 保存员工的工作经历信息 - 批量
    Integer empId = emp.getId();
    List<EmpExpr> exprList = emp.getExprList();
    if(!CollectionUtils.isEmpty(exprList)){
        exprList.forEach(empExpr -> empExpr.setEmpId(empId));
        empExprMapper.insertBatch(exprList);
    }
}

```

**2). EmpExprMapper**

```
@Mapper
public interface EmpExprMapper {

    /**
     * 批量插入员工工作经历信息
     */
    public void insertBatch(List<EmpExpr> exprList);
}

```

**3). EmpExprMapper.xml**

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.itheima.mapper.EmpExprMapper">

    <!--批量插入员工工作经历信息-->
    <insert id="insertBatch">
        insert into emp_expr (emp_id, begin, end, company, job) values
        <foreach collection="exprList" item="expr" separator=",">
            (#{expr.empId}, #{expr.begin}, #{expr.end}, #{expr.company}, #{expr.job})
        </foreach>
    </insert>

</mapper>

```

这里用到Mybatis中的动态SQL里提供的 `<foreach>` 标签，改标签的作用，是用来遍历循环，常见的属性说明：

1. collection：集合名称
2. item：集合遍历出来的元素/项
3. separator：每一次遍历使用的分隔符
4. open：遍历开始前拼接的片段
5. close：遍历结束后拼接的片段

上述的属性，是可选的，并不是所有的都是必须的。 可以自己根据实际需求，来指定对应的属性。

#### 1.6 前后端联调

功能测试通过后，我们再进行通过打开浏览器，测试后端功能接口：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/af35cdf93ed540f8b2142c2767ff3a46.png)  
 点击保存之后，可以看到列表中已经展示出了这条数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/853448d8a8004edf9673cafb96423ffc.png)

### 3. 文件上传

在我们完成的 新增员工 功能中，还存在一个问题：没有头像(图片缺失)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/08f274d4583c40b9bf51c3af6f52f074.png)

上述问题，需要我们通过文件上传技术来解决。下面我们就进入到文件上传技术的学习。

文件上传技术这块我们主要讲解三个方面：首先我们先对文件上传做一个整体的介绍，接着再学习文件上传的本地存储方式，最后学习云存储方式。

接下来我们就先来学习下什么是文件上传。

#### 3.1 简介

文件上传，是指将本地图片、视频、音频等文件上传到服务器，供其他用户浏览或下载的过程。

文件上传在项目中应用非常广泛，我们经常发微博、发微信朋友圈都用到了文件上传功能。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/055163b8f7354bd28c812c9eb2db209a.png)  
 在我们的案例中，在新增员工的时候，要上传员工的头像，此时就会涉及到文件上传的功能。在进行文件上传时，我们点击加号或者是点击图片，就可以选择手机或者是电脑本地的图片文件了。当我们选择了某一个图片文件之后，这个文件就会上传到服务器，从而完成文件上传的操作

想要完成文件上传这个功能需要涉及到两个部分：

1. 前端程序
2. 服务端程序  
    我们先来看看在前端程序中要完成哪些代码：

```
<form action="/upload" method="post" enctype="multipart/form-data">
	姓名: <input type="text" name="username"><br>
    年龄: <input type="text" name="age"><br>
    头像: <input type="file" name="file"><br>
    <input type="submit" value="提交">
</form>

```

上传文件的原始form表单，要求表单必须具备以下三点（上传文件页面三要素）：

* 表单必须有file域，用于选择要上传的文件

  > ```
  > <input type="file" name="file"/>
  >
  > ```
* 表单提交方式必须为POST

  > 通常上传的文件会比较大，所以需要使用 POST 提交方式
* 表单的编码类型enctype必须要设置为：multipart/form-data

  > 普通默认的编码格式是不适合传输大型的二进制数据的，所以在文件上传时，表单的编码格式必须设置为multipart/form-data

前端页面的3要素我们了解后，接下来我们就来验证下所讲解的文件上传3要素。

在提供的"课程资料"中有一个名叫"文件上传"的文件夹，直接将里的"upload.html"文件，复制到springboot项目工程下的static目录里面。

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201105071.png&pos_id=img-qGUDJFL3-1735221400048)

下面我们来验证：删除form表单中 `enctype` 属性值，会是什么情况？

1). 在IDEA中直接使用浏览器打开upload.html页面

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201128257.png&pos_id=img-5ezBPNBx-1735221400049)

2). 选择要上传的本地文件

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201147197.png&pos_id=img-2vGxemzY-1735221400049)

3). 点击"提交"按钮，进入到开发者模式观察

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201208117.png&pos_id=img-0BkJZQvX-1735221400049)

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201224027.png&pos_id=img-84WQsRTH-1735221400049)

我们再来验证：设置form表单中enctype属性值为 `multipart/form-data`，会是什么情况？

```
 <form action="/upload" method="post" enctype="multipart/form-data">
        姓名: <input type="text" name="username"><br>
        年龄: <input type="text" name="age"><br>
        头像: <input type="file" name="file"><br>
        <input type="submit" value="提交">
    </form>

```

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201310392.png&pos_id=img-NfjgUXYD-1735221400049)

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201326218.png&pos_id=img-8sLdw2bw-1735221400049)

知道了前端程序中需要设置上传文件页面三要素，那我们的后端程序又是如何实现的呢？

* 首先在服务端定义这么一个controller，用来进行文件上传，然后在controller当中定义一个方法来处理`/upload` 请求
* 在定义的方法中接收提交过来的数据 （方法中的形参名和请求参数的名字保持一致）

  + 用户名：String name
  + 年龄： Integer age
  + 文件： MultipartFile file
  > Spring中提供了一个API：MultipartFile，使用这个API就可以来接收到上传的文件

![image-20231203201417856](assets/image-20231203201417856.png)
> 问题：如果表单项的名字和方法中形参名不一致，该怎么办？
>
> * ```
>   public Result upload(String username,
>                        Integer age, 
>                        MultipartFile image) //image形参名和请求参数名file不一致
>
>   ```
>
> 解决：使用@RequestParam注解进行参数绑定
>
> * ```
>   public Result upload(String username,
>                        Integer age, 
>                        @RequestParam("file") MultipartFile image)
>
>   ```

**UploadController代码：**

```
@Slf4j
@RestController
public class UploadController {

    @PostMapping("/upload")
    public Result upload(String username, Integer age, MultipartFile file)  {
        log.info("文件上传：{},{},{}",username,age,file);
        return Result.success();
    }

}

```

后端程序编写完成之后，打个断点，以debug方式启动SpringBoot项目

打开浏览器输入：http://localhost:8080/upload.html ， 录入数据并提交

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201525074.png&pos_id=img-cVHRFFAQ-1735221400049)

通过后端程序控制台可以看到，上传的文件是存放在一个临时目录

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201539826.png&pos_id=img-NNntJ9Ss-1735221400049)

打开临时目录可以看到以下内容：

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201555919.png&pos_id=img-jq0A0S6O-1735221400050)

表单提交的三项数据(姓名、年龄、文件)，分别存储在不同的临时文件中：

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203201614000.png&pos_id=img-OnGQyvGx-1735221400050)

> 当我们程序运行完毕之后，这个临时文件会自动删除。
>
> 所以，我们如果想要实现文件上传，需要将这个临时文件，要转存到我们的磁盘目录中。

#### 3.2 本地存储

前面我们已分析了文件上传功能前端和后端的基础代码实现，文件上传时在服务端会产生一个临时文件，请求响应完成之后，这个临时文件被自动删除，并没有进行保存。下面呢，我们就需要完成将上传的文件保存在服务器的本地磁盘上。

代码实现：

1. 在服务器本地磁盘上创建images目录，用来存储上传的文件（例：E盘创建images目录）
2. 使用 MultipartFile 类提供的API方法，把临时文件转存到本地磁盘目录下

> MultipartFile 常见方法：
>
> * String getOriginalFilename(); //获取原始文件名
> * void transferTo(File dest); //将接收的文件转存到磁盘文件中
> * long getSize(); //获取文件的大小，单位：字节
> * byte[] getBytes(); //获取文件内容的字节数组
> * InputStream getInputStream(); //获取接收到的文件内容的输入流

```
@RestController
public class UploadController {
    @PostMapping("/upload")    
    public Result upload(MultipartFile file) throws IOException {
        //获取原始文件名
        String originalFilename = file.getOriginalFilename();
        //构建新的文件名
        String newFileName = UUID.randomUUID().toString()+originalFilename.substring(originalFilename.lastIndexOf("."));
        //将文件保存在服务器端 D:/images/ 目录下
        file.transferTo(new File("D:/images/"+newFileName));
        return Result.success();
    }
}

```

利用 `Apifox` 测试：

注意：请求参数名和controller方法形参名保持一致

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203202449019.png&pos_id=img-IBOiKR4i-1735221400050)

通过 `Apifox` 测试，我们发现文件上传是没有问题的。

在解决了文件名唯一性的问题后，我们再次上传一个较大的文件(超出1M)时发现，后端程序报错：

![外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传](https://img-home.csdnimg.cn/images/20230724024159.png?origin_url=assets%2Fimage-20231203203317543.png&pos_id=img-Ln51t6TT-1735221400050)

报错原因呢，是因为：在SpringBoot中，文件上传时默认单个文件最大大小为1M

那么如果需要上传大文件，可以在 `application.properties` 进行如下配置：

```
#配置单个文件最大上传大小
spring.servlet.multipart.max-file-size=10MB

#配置单个请求最大上传大小(一次请求可以上传多个文件)
spring.servlet.multipart.max-request-size=100MB

```

到时此，我们文件上传的本地存储方式已完成了。但是这种本地存储方式还存在一问题：

![image-20231203203412212](assets/image-20231203203412212.png)

如果直接存储在服务器的磁盘目录中，存在以下缺点：

* 不安全：磁盘如果损坏，所有的文件就会丢失
* 容量有限：如果存储大量的图片，磁盘空间有限(磁盘不可能无限制扩容)
* 无法直接访问

为了解决上述问题呢，通常有两种解决方案：

* 自己搭建存储服务器，如：fastDFS 、MinIO
* 使用现成的云服务，如：阿里云，腾讯云，华为云

#### 3.3 阿里云OSS

##### 3.3.1 准备

阿里云是阿里巴巴集团旗下全球领先的云计算公司，也是国内最大的云服务提供商 。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/49201cbbb125417b9b0f91b2fc46c11e.png)

云服务指的就是通过互联网对外提供的各种各样的服务，比如像：语音服务、短信服务、邮件服务、视频直播服务、文字识别服务、对象存储服务等等。

当我们在项目开发时需要用到某个或某些服务，就不需要自己来开发了，可以直接使用阿里云提供好的这些现成服务就可以了。比如：在项目开发当中，我们要实现一个短信发送的功能，如果我们项目组自己实现，将会非常繁琐，因为你需要和各个运营商进行对接。而此时阿里云完成了和三大运营商对接，并对外提供了一个短信服务。我们项目组只需要调用阿里云提供的短信服务，就可以很方便的来发送短信了。这样就降低了我们项目的开发难度，同时也提高了项目的开发效率。（大白话：别人帮我们实现好了功能，我们只要调用即可）

云服务提供商给我们提供的软件服务通常是需要收取一部分费用的。

阿里云对象存储OSS（Object Storage Service），是一款海量、安全、低成本、高可靠的云存储服务。使用OSS，您可以通过网络随时存储和调用包括文本、图片、音频和视频等在内的各种文件。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a44acf2b42e44dbd9259b512941866ee.png)  
 在我们使用了阿里云OSS对象存储服务之后，我们的项目当中如果涉及到文件上传这样的业务，在前端进行文件上传并请求到服务端时，在服务器本地磁盘当中就不需要再来存储文件了。我们直接将接收到的文件上传到oss，由 oss帮我们存储和管理，同时阿里云的oss存储服务还保障了我们所存储内容的安全可靠。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/07f9c311d27a4a2b89684784c98bec49.png)  
 那我们学习使用这类云服务，我们主要学习什么呢？其实我们主要学习的是如何在项目当中来使用云服务完成具体的业务功能。而无论使用什么样的云服务，阿里云也好，腾讯云、华为云也罢，在使用第三方的服务时，操作的思路都是一样的。

SDK：Software Development Kit 的缩写，软件开发工具包，包括辅助软件开发的依赖（jar包）、代码示例等，都可以叫做SDK。

简单说，sdk中包含了我们使用第三方云服务时所需要的依赖，以及一些示例代码。我们可以参照sdk所提供的示例代码就可以完成入门程序。

第三方服务使用的通用思路，我们做一个简单介绍之后，接下来我们就来介绍一下我们当前要使用的阿里云oss对象存储服务具体的使用步骤。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3d1ac3aa095b46afb18d927bef7bf47f.png)

Bucket：存储空间是用户用于存储对象（Object，就是文件）的容器，所有的对象都必须隶属于某个存储空间。

###### 3.3.1.1 账号准备

下面我们根据之前介绍的使用步骤，完成准备工作：

1. 注册阿里云账户（**注册完成后需要实名认证**）

   https://account.aliyun.com/login/login.htmoauth\_callback=https%3A%2F%2Fwww.aliyun.com%2F

[添加链接描述](#####%203.3.1.1%20%E8%B4%A6%E5%8F%B7%E5%87%86%E5%A4%87%20%20%E4%B8%8B%E9%9D%A2%E6%88%91%E4%BB%AC%E6%A0%B9%E6%8D%AE%E4%B9%8B%E5%89%8D%E4%BB%8B%E7%BB%8D%E7%9A%84%E4%BD%BF%E7%94%A8%E6%AD%A5%E9%AA%A4%EF%BC%8C%E5%AE%8C%E6%88%90%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C%EF%BC%9A%20%201.%20%E6%B3%A8%E5%86%8C%E9%98%BF%E9%87%8C%E4%BA%91%E8%B4%A6%E6%88%B7%EF%BC%88**%E6%B3%A8%E5%86%8C%E5%AE%8C%E6%88%90%E5%90%8E%E9%9C%80%E8%A6%81%E5%AE%9E%E5%90%8D%E8%AE%A4%E8%AF%81**%EF%BC%89%20%20%20%20%20https://account.aliyun.com/login/login.htm?oauth_callback=https://www.aliyun.com/)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ee4cbbc58d974dd29ca82cac8b4074ef.png)

###### 3.3.1.2 开通OSS云服务

1). 通过控制台找到对象存储O![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cf4a233346924247b825d429448f7dbd.png)  
 SS服务

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e38de23a260c42a183248b803fe98537.png)  
 如果是第一次访问，还需要开通对象存储服务OSS

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a68fdb13a3a94dad83e79febb99b34ad.png)  
 2). 开通OSS服务之后，就可以进入到阿里云对象存储的控制台

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7793427e601b409c8404f8daf3bc0989.png)  
 3). 点击左侧的 “Bucket列表”，创建一个Bucket

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e8ef02e69892404588ee3eb08fcc1f84.png)

###### 3.3.1.3 配置AK & SK

1). 创建AccessKey

点击 “AccessKey管理”，进入到管理页面。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0220b762cdd44bcb9947d33b0f81d745.png)  
 点击 “AccessKey”。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b4e9ea1bf52a434ba56111bacec6bb9f.png)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ef8f73708fb94f4c9f57a39bb4096617.png)  
 2). 配置AK & SK

以**管理员身份**打开CMD命令行，执行如下命令，配置系统的环境变量。

```
set OSS_ACCESS_KEY_ID=LTAI5tXXXXXXXXXXXXXXXXXXXXM8TP
set OSS_ACCESS_KEY_SECRET=UzMcJXXXXXXXXXXXXXXXXXXXXdabTNafi

```

注意：将上述的ACCESS\_KEY\_ID 与 ACCESS\_KEY\_SECRET 的值一定一定一定一定一定一定要替换成自己的 。

执行如下命令，让更改生效。

```
setx OSS_ACCESS_KEY_ID "%OSS_ACCESS_KEY_ID%"
setx OSS_ACCESS_KEY_SECRET "%OSS_ACCESS_KEY_SECRET%"

```

执行如下命令，验证环境变量是否生效。

```
echo %OSS_ACCESS_KEY_ID%
echo %OSS_ACCESS_KEY_SECRET%

```

##### 3.3.3 集成

###### 3.3.3.1 介绍

阿里云oss对象存储服务的准备工作以及入门程序我们都已经完成了，接下来我们就需要在案例当中集成oss对象存储服务，来存储和管理案例中上传的图片。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/aa33ad3ea01e4fb2940093e329ea1b37.png)

> 在新增员工的时候，上传员工的图像，而之所以需要上传员工的图像，是因为将来我们需要在系统页面当中访问并展示员工的图像。而要想完成这个操作，需要做两件事：
>
> 1. 需要上传员工的图像，并把图像保存起来（存储到阿里云OSS）
> 2. 访问员工图像（通过图像在阿里云OSS的存储地址访问图像）
>    * OSS中的每一个文件都会分配一个访问的url，通过这个url就可以访问到存储在阿里云上的图片。所以需要把url返回给前端，这样前端就可以通过url获取到图像。

###### 3.3.3.2 实现

1). 引入阿里云OSS上传文件工具类（由官方的示例代码改造而来）

```
/**
 * 阿里云OSS操作工具类
 */
@Slf4j
public class AliyunOSSUtils {

    /**
     * 上传文件
     * @param endpoint endpoint域名
     * @param bucketName 存储空间的名字
     * @param content 内容字节数组
     */
    public static String upload(String endpoint, String bucketName, byte[] content, String extName) throws Exception {
        // 从环境变量中获取访问凭证。运行本代码示例之前，请确保已设置环境变量OSS_ACCESS_KEY_ID和OSS_ACCESS_KEY_SECRET。
        EnvironmentVariableCredentialsProvider credentialsProvider = CredentialsProviderFactory.newEnvironmentVariableCredentialsProvider();
        // 填写Object完整路径，完整路径中不能包含Bucket名称，例如exampledir/exampleobject.txt。
        String objectName = UUID.randomUUID() + extName;

        // 创建OSSClient实例。
        OSS ossClient = new OSSClientBuilder().build(endpoint, credentialsProvider);
        try {
            // 创建PutObjectRequest对象。
            PutObjectRequest putObjectRequest = new PutObjectRequest(bucketName, objectName, new ByteArrayInputStream(content));
            // 创建PutObject请求。
            PutObjectResult result = ossClient.putObject(putObjectRequest);
        } catch (OSSException oe) {
            log.error("Caught an OSSException, which means your request made it to OSS, but was rejected with an error response for some reason.");
            log.error("Error Message:" + oe.getErrorMessage());
            log.error("Error Code:" + oe.getErrorCode());
            log.error("Request ID:" + oe.getRequestId());
            log.error("Host ID:" + oe.getHostId());
        } catch (ClientException ce) {
            log.error("Caught an ClientException, which means the client encountered a serious internal problem while trying to communicate with OSS, such as not being able to access the network.");
            log.error("Error Message:" + ce.getMessage());
        } finally {
            if (ossClient != null) {
                ossClient.shutdown();
            }
        }

        return endpoint.split("//")[0] + "//" + bucketName + "." + endpoint.split("//")[1] + "/" + objectName;
    }

}

```

2). 修改UploadController代码：

```
@Slf4j
@RestController
public class UploadController {
    private String endpoint = "https://oss-cn-beijing.aliyuncs.com";
    private String bucketName = "java417-web";
	
    @PostMapping("/upload")
    public Result upload(MultipartFile file) throws Exception {
        log.info("文件上传: {}", file.getOriginalFilename());
        String extName = file.getOriginalFilename().substring(file.getOriginalFilename().lastIndexOf("."));
        String url = AliyunOSSUtils.upload(endpoint, bucketName, file.getBytes(), extName);
        return Result.success(url);
    }

}

```

### 4. 配置文件

员工管理的新增功能我们已开发完成，但在我们所开发的程序中还一些小问题，下面我们就来分析一下当前案例中存在的问题以及如何优化解决。

#### 4.1 参数配置化

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e5c470feda2e4fd3afb73d10ce4fc1b0.png)在我们之前编写的程序中进行文件上传时，需要指定两个参数：

* endpoint //阿里云OSS域名
* bucket //存储空间的名字

关于以上的这些阿里云相关配置信息，我们是直接写死在java代码中了(硬编码)，如果我们在做项目时每涉及到一个第三方技术服务，就将其参数硬编码，那么在Java程序中会存在两个问题：

1. 如果这些参数发生变化了，就必须在源程序代码中改动这些参数，然后需要重新进行代码的编译，将Java代码编译成class字节码文件再重新运行程序。（比较繁琐）
2. 如果我们开发的是一个真实的企业级项目， Java类可能会有很多，如果将这些参数分散的定义在各个Java类当中，我们要修改一个参数值，我们就需要在众多的Java代码当中来定位到对应的位置，再来修改参数，修改完毕之后再重新编译再运行。（参数配置过于分散，是不方便集中的管理和维护）  
    为了解决以上分析的问题，我们可以将参数配置在配置文件中。如下：

```
#自定义的阿里云OSS配置信息
aliyun.oss.endpoint=https://oss-cn-beijing.aliyuncs.com
aliyun.oss.bucketName=java417-web

```

在将阿里云OSS配置参数交给properties配置文件来管理之后，我们的 UploadController 就变为以下形式：

```
@Slf4j
@RestController
public class UploadController {
    
    private String endpoint;
    private String bucketName;

    @PostMapping("/upload")
    public Result upload(MultipartFile file) throws Exception {
        log.info("文件上传: {}", file.getOriginalFilename());
        String extName = file.getOriginalFilename().substring(file.getOriginalFilename().lastIndexOf("."));
        String url = AliyunOSSUtils.upload(endpoint, bucketName, file.getBytes(), extName);
        return Result.success(url);
    }

}

```

> 而此时如果直接调用 UploadController 类当中的upload方法进行文件上传时，这2项参数全部为null，原因是因为并没有给它赋值。
>
> 此时我们是不是需要将配置文件当中所配置的属性值读取出来，并分别赋值给 UploadController 当中的各个属性呢？那应该怎么做呢？  
>  因为 `application.properties` 是springboot项目默认的配置文件，所以springboot程序在启动时会默认读取 `application.properties` 配置文件，而我们可以使用一个现成的注解：`@Value`，获取配置文件中的数据。

`@Value` 注解通常用于外部配置的属性注入，具体用法为： `@Value("${配置文件中的key}")`

```
@Slf4j
@RestController
public class UploadController {
	
    @Value("${aliyun.oss.endpoint}")
    private String endpoint;
    @Value("${aliyun.oss.bucketName}")
    private String bucketName;

    @PostMapping("/upload")
    public Result upload(MultipartFile file) throws Exception {
        log.info("文件上传: {}", file.getOriginalFilename());
        String extName = file.getOriginalFilename().substring(file.getOriginalFilename().lastIndexOf("."));
        String url = AliyunOSSUtils.upload(endpoint, bucketName, file.getBytes(), extName);
        return Result.success(url);
    }

}

```

具体的加载流程如下:

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7af95c15d16f489994fc7fe5d4fe012e.png)

## 员工信息-删除&修改

前面我们已经实现了员工信息的条件分页查询以及新增操作。 关于员工管理的功能，还有两个需要实现：

* 删除员工
* 修改员工

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/66ee0c65fcb34bf7a27e7b65e307f52a.png)  
 除了员工管理的功能之外，我们还要再完成员工信息统计的功能开发。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/af55d60697ca41e497a42845d9616495.png)  
 首先我们先完成 “删除员工” 的功能开发，再完成 “修改员工” 的功能开发。再来完成员工信息统计的接口开发 。

综上所述，我们今天的课程内容包含以下四个部分：

* 删除员工
* 修改员工
* 异常处理
* 员工信息统计

### 1. 删除员工

#### 3.3.1 需求

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/090598fd09d241a3a5179d9df1c0598e.png)  
 当我们勾选列表前面的复选框，然后点击 “批量删除” 按钮，就可以将这一批次的员工信息删除掉了。也可以只勾选一个复选框，仅删除一个员工信息。

问题：我们需要开发两个功能接口吗？一个删除单个员工，一个删除多个员工

答案：不需要。 只需要开发一个功能接口即可（删除多个员工包含只删除一个员工）

#### 3.3.4 功能开发

##### 3.3.4.1 Controller接收参数

在 `EmpController` 中增加如下方法 `delete` ，来执行批量删除员工的操作。

**方式一：在Controller方法中通过数组来接收**

多个参数，默认可以将其封装到一个数组中，需要保证前端传递的参数名 与 方法形参名称保持一致。

```
/**
* 批量删除员工
*/
@DeleteMapping
public Result delete(Integer[] ids){
    log.info("批量删除部门: ids={} ", Arrays.asList(ids));
    return Result.success();
}

```

**方式二：在Controller方法中通过集合来接收**

也可以将其封装到一个List 集合中，如果要将其封装到一个集合中，需要在集合前面加上 `@RequestParam` 注解。

```
/**
* 批量删除员工
*/
@DeleteMapping
public Result delete(@RequestParam List<Integer> ids){
    log.info("批量删除部门: ids={} ", ids);
    empService.deleteByIds(ids);
    return Result.success();
}

```

两种方式，选择其中一种就可以，我们一般推荐选择集合，因为基于集合操作其中的元素会更加方便。

##### 3.3.4.2 Service

1). 在接口中 `EmpService` 中定义接口方法 `deleteByIds`

```
/**
* 批量删除员工
*/
void deleteByIds(List<Integer> ids);

```

2). 在实现类 `EmpServiceImpl` 中实现接口方法 `deleteByIds`

在删除员工信息时，既需要删除 emp 表中的员工基本信息，还需要删除 emp\_expr 表中员工的工作经历信息

```
@Transactional
@Override
public void deleteByIds(List<Integer> ids) {
    //1. 根据ID批量删除员工基本信息
    empMapper.deleteByIds(ids);

    //2. 根据员工的ID批量删除员工的工作经历信息
    empExprMapper.deleteByEmpIds(ids);
}

```

**由于删除员工信息，既要删除员工基本信息，又要删除工作经历信息，操作多次数据库的删除，所以需要进行事务控制。**

##### 3.3.4.3 Mapper

1). 在 `EmpMapper` 接口中增加 `deleteByIds` 方法实现批量删除员工基本信息

```
/**
* 批量删除员工信息
*/
void deleteByIds(List<Integer> ids);

```

2). 在 `EmpMapper.xml` 配置文件中, 配置对应的SQL语句

```
<!--批量删除员工信息-->
<delete id="deleteByIds">
    delete from emp where id in
    <foreach collection="ids" item="id" open="(" close=")" separator=",">
    	#{id}
    </foreach>
</delete>

```

3). 在 `EmpExprMapper` 接口中增加 `deleteByEmpIds` 方法实现根据员工ID批量删除员工的工作经历信息

```
/**
* 根据员工的ID批量删除工作经历信息
*/
void deleteByEmpIds(List<Integer> empIds);

```

4). 在 `EmpExprMapper.xml` 配置文件中, 配置对应的SQL语句

```
<!--根据员工的ID批量删除工作经历信息-->
<delete id="deleteByEmpIds">
    delete from emp_expr where emp_id in
    <foreach collection="empIds" item="empId" open="(" close=")" separator=",">
    	#{empId}
    </foreach>
</delete>

```

#### 3.3.6 前后端联调

打开浏览器，测试后端功能接口：![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bdf48055ab7a49d49eb57de8ece0496f.png)

### 2. 修改员工

需求：修改员工信息

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ac993f74d7f347678047ae46345446f9.png)  
 在进行修改员工信息的时候，我们首先先要根据员工的ID查询员工的详细信息用于页面回显展示，然后用户修改员工数据之后，点击保存按钮，就可以将修改的数据提交到服务端，保存到数据库。 具体操作为：

1. 根据ID查询员工信息
2. 保存修改的员工信息

##### 2.1.2 实现思路

在查询回显时，既需要查询出员工的基本信息，又需要查询出该员工的工作经历信息。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/25cc780546b34a5a81ea48cdb91c3493.png)

##### 2.1.3 代码实现

1). `EmpController` 添加 `getInfo` 用来根据ID查询员工数据，用于页面回显

```
/**
 * 查询回显
 */
@GetMapping("/{id}")
public Result getInfo(@PathVariable Integer id){
    log.info("根据id查询员工的详细信息");
    Emp emp  = empService.getInfo(id);
    return Result.success(emp);
}

```

2). `EmpService` 接口中增加 `getInfo` 方法

```
/**
 * 根据ID查询员工的详细信息
 */
Emp getInfo(Integer id);

```

3). `EmpServiceImpl` 实现类中实现 `getInfo` 方法

```
@Override
public Emp getInfo(Integer id) {
    return empMapper.getById(id);
}

```

4). `EmpMapper` 接口中增加 `getById` 方法

```
/**
 * 根据ID查询员工详细信息
 */
Emp getById(Integer id);

```

5). `EmpMapper.xml` 配置文件中定义对应的SQL

```
<!--自定义结果集ResultMap-->
<resultMap id="empResultMap" type="com.itheima.pojo.Emp">
    <id column="id" property="id" />
    <result column="username" property="username" />
    <result column="password" property="password" />
    <result column="name" property="name" />
    <result column="gender" property="gender" />
    <result column="phone" property="phone" />
    <result column="job" property="job" />
    <result column="salary" property="salary" />
    <result column="image" property="image" />
    <result column="entry_date" property="entryDate" />
    <result column="dept_id" property="deptId" />
    <result column="create_time" property="createTime" />
    <result column="update_time" property="updateTime" />

    <!--封装exprList-->
    <collection property="exprList" ofType="com.itheima.pojo.EmpExpr">
        <id column="ee_id" property="id"/>
        <result column="ee_company" property="company"/>
        <result column="ee_job" property="job"/>
        <result column="ee_begin" property="begin"/>
        <result column="ee_end" property="end"/>
        <result column="ee_empid" property="empId"/>
    </collection>
</resultMap>

<!--根据ID查询员工的详细信息-->
<select id="getById" resultMap="empResultMap">
    select e.*,
        ee.id ee_id,
        ee.emp_id ee_empid,
        ee.begin ee_begin,
        ee.end ee_end,
        ee.company ee_company,
        ee.job ee_job
    from emp e left join emp_expr ee on e.id = ee.emp_id
    where e.id = #{id}
</select>

```

在这种一对多的查询中，我们要想成功的封装的结果，需要手动的基于 `<resultMap>` 来进行封装结果。

> * Mybatis中封装查询结果，什么时候用 resultType，什么时候用resultMap ？
>   + 如果查询返回的字段名与实体的属性名可以直接对应上，用resultType 。
>   + 如果查询返回的字段名与实体的属性名对应不上，或实体属性比较复杂，可以通过resultMap手动封装 。

##### 2.1.5 前后端联调测试

打开浏览器，进行前后端联调测试。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f5b7bc2c2f1c421cb36b8a260758332d.png)

#### 2.2 修改员工

查询回显之后，就可以在页面上修改员工的信息了。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fc9a8fd91e2c47f98ca6fd146d336dae.png)

> 当用户修改完数据之后，点击保存按钮，就需要将数据提交到服务端，然后服务端需要将修改后的数据更新到数据库中 。
>
> 而此次更新的时候，既需要更新员工的基本信息； 又需要更新员工的工作经历信息 。

##### 2.2.3 代码实现

1). `EmpController` 增加 `update` 方法接收请求参数，响应数据

```
/**
* 更新员工信息
*/
@PutMapping
public Result update(@RequestBody Emp emp){
    log.info("修改员工信息, {}", emp);
    empService.update(emp);
    return Result.success();
}

```

2). `EmpService` 接口增加 `update` 方法

```
/**
* 更新员工信息
* @param emp
*/
void update(Emp emp);

```

3). `EmpServiceImpl` 实现类实现 `update` 方法

```
@Transactional
@Override
public void update(Emp emp) {
    //1. 根据ID更新员工基本信息
    emp.setUpdateTime(LocalDateTime.now());
    empMapper.updateById(emp);

    //2. 根据员工ID删除员工的工作经历信息 【删除老的】
    empExprMapper.deleteByEmpIds(Arrays.asList(emp.getId()));

    //3. 新增员工的工作经历数据 【新增新的】
    Integer empId = emp.getId();
    List<EmpExpr> exprList = emp.getExprList();
    if(!CollectionUtils.isEmpty(exprList)){
        exprList.forEach(empExpr -> empExpr.setEmpId(empId));
        empExprMapper.insertBatch(exprList);
    }
}

```

4). `EmpMapper` 接口中增加 `updateById` 方法

```
/**
* 更新员工基本信息
*/
void updateById(Emp emp);

```

5). `EmpMapper.xml` 配置文件中定义对应的SQL语句，基于动态SQL更新员工信息

```
<!--根据ID更新员工信息-->
<update id="updateById">
    update emp
    <set>
        <if test="username != null and username != ''">username = #{username},</if>
        <if test="password != null and password != ''">password = #{password},</if>
        <if test="name != null and name != ''">name = #{name},</if>
        <if test="gender != null">gender = #{gender},</if>
        <if test="phone != null and phone != ''">phone = #{phone},</if>
        <if test="job != null">job = #{job},</if>
        <if test="salary != null">salary = #{salary},</if>
        <if test="image != null and image != ''">image = #{image},</if>
        <if test="entryDate != null">entry_date = #{entryDate},</if>
        <if test="deptId != null">dept_id = #{deptId},</if>
        <if test="updateTime != null">update_time = #{updateTime},</if>
    </set>
    where id = #{id}
</update>

```

2.2.5 前后端联调测试

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/24a0f7d4550b489faa365f9f90cfa77b.png)  
 点击保存之后，查看更新后的数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/71b6f23d7f724d5bbf6921f9d256b475.png)

### 4. 员工信息统计

员工管理的增删改查功能我们已开发完成，接下来，我们再来完成员工信息统计的接口开发。 对于这些图形报表的开发，其实呢，都是基于现成的一些图形报表的组件开发的，比如：Echarts、HighCharts等。

而报表的制作，主要是前端人员开发，引入对应的组件（比如：ECharts）即可。 服务端开发人员仅为其提供数据即可。

官网：https://echarts.apache.org/zh/index.html

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/298b3b75747f4547ad1d8d6d3cf094f2.png)

#### 4.1 职位统计

##### 4.1.1 需求

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0fe96183c7a34adda99e1cb02070e95c.png)  
 对于这类的图形报表，服务端要做的，就是为其提供数据即可。 我们可以通过官方的示例，看到提供的数据其实就是X轴展示的信息，和对应的数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4539b9b88811425a9a5c39af5c027fe4.png)  
 **3). 响应数据**

参数格式：application/json

参数说明：

| 参数名 | 类型 | 是否必须 | 备注 |
| --- | --- | --- | --- |
| code | number | 必须 | 响应码，1 代表成功，0 代表失败 |
| msg | string | 非必须 | 提示信息 |
| data | object | 非必须 | 返回的数据 |
| |- jobList | string[] | 必须 | 职位列表 |
| |- dataList | number[] | 必须 | 人数列表 |

响应数据样例：

```
{
  "code": 1,
  "msg": "success",
  "data": {
    "jobList": ["教研主管","学工主管","其他","班主任","咨询师","讲师"],
    "dataList": [1,1,2,6,8,13]
  }
}

```

为了封装上面需要给前端返回的数据，在pojo包下再创建一个实体类 `JobOption`，封装给前端返回的结果：

```
/**
 * 员工职位人数统计
 */
@Data
@NoArgsConstructor
@AllArgsConstructor
public class JobOption {
    private List jobList; //职位列表
    private List dataList; //人数列表
}

```

##### 4.1.3 代码实现

**1). 定义ReportController，并添加方法。**

```
@Slf4j
@RequestMapping("/report")
@RestController
public class ReportController {

    @Autowired
    private ReportService reportService;

    /**
     * 统计各个职位的员工人数
     */
    @GetMapping("/empJobData")
    public Result getEmpJobData(){
        log.info("统计各个职位的员工人数");
        JobOption jobOption = reportService.getEmpJobData();
        return Result.success(jobOption);
    }
}

```

**2). 定义ReportService接口，并添加接口方法。**

```
public interface ReportService {
    /**
     * 统计各个职位的员工人数
     * @return
     */
    JobOption getEmpJobData();
}

```

**3). 定义ReportServiceImpl实现类，并实现方法**

```
@Service
public class ReportServiceImpl implements ReportService {

    @Autowired
    private EmpMapper empMapper;
	
    @Override
    public JobOption getEmpJobData() {
        List<Map<String,Object>> list = empMapper.countEmpJobData();
        List<Object> jobList = list.stream().map(dataMap -> dataMap.get("pos")).toList();
        List<Object> dataList = list.stream().map(dataMap -> dataMap.get("total")).toList();
        return new JobOption(jobList, dataList);
    }
}

```

**4). 定义EmpMapper 接口**

统计的是员工的信息，所以需要操作的是员工表。 所以代码我们就写在 `EmpMapper` 接口中即可。

```
/**
 * 统计各个职位的员工人数
 */
@MapKey("pos")
List<Map<String,Object>> countEmpJobData();

```

> 如果查询的记录往Map中封装，可以通过@MapKey注解指定返回的map中的唯一标识是那个字段。【也可以不指定】

**5). 定义EmpMapper.xml**

```
<!-- 统计各个职位的员工人数 -->
<select id="countEmpJobData" resultType="java.util.Map">
    select
    (case job when 1 then '班主任' 
    		 when 2 then '讲师' 
    		 when 3 then '学工主管' 
    		 when 4 then '教研主管' 
    		 when 5 then '咨询师' 
    		 else '其他' end)  pos,
    count(*) total
    from emp group by job
    order by total
</select>

```

> **case流程控制函数：**
>
> * 语法一：case when cond1 then res1 [ when cond2 then res2 ] else res end ;
>
>   + 含义：如果 cond1 成立， 取 res1。 如果 cond2 成立，取 res2。 如果前面的条件都不成立，则取 res。
> * 语法二（仅适用于等值匹配）：case expr when val1 then res1 [ when val2 then res2 ] else res end ;
>
>   + 含义：如果 expr 的值为 val1 ， 取 res1。 如果 expr 的值为 val2 ，取 res2。 如果前面的条件都不成立，则取 res。

##### 4.1.5 联调测试

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a44abcf05f694d57a1c9f14822921eb9.png)

#### 4.2 性别统计

##### 4.2.1 需求在这里插入图片描述

对于这类的图形报表，服务端要做的，就是为其提供数据即可。 我们可以通过官方的示例，看到提供的数据就是一个json格式的数据。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0493ac6d5db046dd9085088bd11fa686.png)

##### 4.2.3 代码实现

**1). 在ReportController，添加方法。**

```
/**
 * 统计员工性别信息
 */
@GetMapping("/empGenderData")
public Result getEmpGenderData(){
    log.info("统计员工性别信息");
    List<Map> genderList = reportService.getEmpGenderData();
    return Result.success(genderList);
}

```

**2). 在ReportService接口，添加接口方法。**

```
/**
 * 统计员工性别信息
 */
List<Map> getEmpGenderData();

```

**3). 在ReportServiceImpl实现类，实现方法**

```
@Override
public List<Map> getEmpGenderData() {
    return empMapper.countEmpGenderData();
}

```

**4). 定义EmpMapper 接口**

统计的是员工的信息，所以需要操作的是员工表。 所以代码我们就写在 `EmpMapper` 接口中即可。

```
/**
 * 统计员工性别信息
 */
@MapKey("name")
List<Map> countEmpGenderData();

```

**5). 定义EmpMapper.xml**

```
<!-- 统计员工的性别信息 -->
<select id="countEmpGenderData" resultType="java.util.Map">
    select
    if(gender = 1, '男', '女') as name,
    count(*) as value
    from emp group by gender ;
</select>

```

> if函数语法：`if(条件, 条件为true取值, 条件为false取值)`

> ifnull函数语法：`ifnull(expr, val1)` 如果expr不为null，取自身，否则取val1

##### 4.2.5 联调测试‘

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/15b19350a24544c2bc889143a476e616.png)