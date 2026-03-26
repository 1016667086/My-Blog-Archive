先上效果图  
 项目源码：https://download.csdn.net/download/qq\_43055855/89891285  
 [源码地址](https://download.csdn.net/download/qq_43055855/89891285)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3045e58e52a14e549de075bd463f2dd9.png)

手机扫描二维码跳转到指定网页

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6aa2ad8f06d04bfd9b19ef3f0f6eaad1.png)

### 概述

这个项目是一个基于 Java 的二维码生成与解析工具，主要由 QRCodeUtil 和 QRCodeController 两个类组成。它利用了 Google ZXing 库来实现二维码的生成和解析功能，并通过 Spring 框架进行整合，提供了 RESTful API 接口用于生成带有 logo 的二维码。

### 主要功能

生成带有 logo 的二维码：

1. 用户可以传入二维码内容和 logo 文件路径（或字节数组），生成带有指定 logo 的二维码图像。通过设置编码提示类型，包括字符集、错误纠正级别和边距等，确保二维码的可读性和容错性。
2. 计算 logo 在二维码中的合适大小，并将其居中绘制在二维码图像上，使生成的二维码更加美观和具有辨识度。
3. 保存二维码到文件或输出流：
4. 可以将生成的二维码保存到指定的文件目录中，若目录不存在则自动创建。如果未指定文件名，则随机生成一个以当前时间戳命名的 png 格式文件。
5. 也可以将二维码生成到输出流中，并以 Base64 编码的形式返回给客户端，方便在网页等环境中直接使用。
6. 解析二维码内容：提供了两种方式解析二维码内容，分别是解析本地二维码图片文件和解析网络二维码图片地址。通过将图像转换为亮度源，再创建二进制位图，最后使用解码提示类型进行解码，获取二维码中的文本内容。
7. RESTful API 接口：QRCodeController 类提供了一个 POST 请求的接口 /qrCode，接受二维码内容和可选的 logo 文件上传。根据上传的 logo 文件情况，生成带有或不带 logo 的二维码，并将其写入 HttpServletResponse 的输出流中返回给客户端。

### 新建maven项目构建springboot

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2421ab4d9c80435d925df5fedac778f6.png)

### 技术要点

Google ZXing 库的使用：

* 熟练掌握了 `Google ZXing` 库中各种类的使用，如 `MultiFormatWriter` 用于生成二维码的位矩阵，`BitMatrix`表示二维码的位数据，`BufferedImageLuminanceSource` 和 HybridBinarizer用于二维码的解析等。图像处理：
* 利用 Java 的 `BufferedImage` 和 `Graphics2D` 类进行图像处理，包括调整 logo 图像的大小、在二维码图像上绘制 `logo` 等操作。
* 文件操作和输入输出流：使用 `ImageIO` 进行图像文件的读取和写入操作，以及处理文件的存在性检查、目录创建等。同时，熟练运用 `OutputStream` 和 `ByteArrayOutputStream` 等输入输出流进行数据的传输和处理。
* Spring 框架整合：  
   通过 @`RestController` 和 @`Slf4j` 等注解，将该工具整合到 Spring 框架中，方便进行日志记录和提供 `RESTful` API 服务。  
   参数校验和错误处理：  
   在接口方法中对传入的参数进行校验，如检查二维码内容是否为空、上传的文件是否为有效的图片文件等。同时，对可能出现的异常进行了捕获和处理，记录错误日志并返回合适的响应。

### pom.xml文件代码

```

    <!-- 定义这是一个springboot项目 -->
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.1.18.RELEASE</version>
    </parent>

    <!-- 定义这是一个web应用 -->
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-devtools</artifactId>
        </dependency>
        <!-- zxing生成二维码 -->
        <dependency>
            <groupId>com.google.zxing</groupId>
            <artifactId>core</artifactId>
            <version>3.3.3</version>
        </dependency>

        <dependency>
            <groupId>com.google.zxing</groupId>
            <artifactId>javase</artifactId>
            <version>3.3.3</version>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-thymeleaf</artifactId>
        </dependency>
        
    </dependencies>

```

我们需要lombock插件thymeleaf魔板引擎，还有两个核心二维码库  
 zing的core和javase

### 在templates下定义yml文件映射

```
spring:
  thymeleaf:
    prefix: classpath:/templates/

```

在静态资源文件`resources`下的`templates`里边新建一个html文件，注意需自己建文件夹

```
<!DOCTYPE html>
<!-- 声明文档类型 -->
<html lang="en">
<!-- HTML文档头部 -->
<head>
    <!-- 设置字符集为UTF-8 -->
    <meta charset="UTF-8">
    <!-- 页面标题 -->
    <title>二维码生成器</title>
    <!-- 内联样式 -->
    <style type="text/css">
        /* 设置文本区域的字体大小、宽度和高度 */
        textarea {
     
     
            font-size: 30px;
            width: 400px;
            height: 200px;
        }
        /* 设置提示信息的样式，包括颜色和默认不显示 */
        .hint {
     
     
            color: red;
            display: none;
        }
        /* 设置二维码容器的样式，包括居中、最小高度等 */
        .qrCodeContainer {
     
     
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            min-height: 100vh;
            position: relative;
            border: 2px solid sandybrown;
            padding: 20px;
            box-sizing: border-box;
        }
    </style>
    <!-- 引入jQuery库 -->
    <script src="https://cdn.bootcss.com/jquery/2.1.1/jquery.min.js"></script>
    <!-- JavaScript代码 -->
    <script type="text/javascript">
        // 当DOM准备就绪时执行
        $(function () {
     
     
            // 当按钮被点击时触发
            $("button").click(function () {
     
     
                // 获取文本区域的值
                var codeContent = $("textarea").val();
                // 获取文件输入框的DOM元素
                var logoInput = $("#logoInput")[0];
                // 获取用户选择的文件
                var logoFile = logoInput.files[0];
                // 检查二维码内容是否为空
                if (codeContent.trim() === "") {
     
     
                    // 显示提示信息
                    $(".hint").text("二维码内容不能为空").fadeIn(500);
                } else {
     
     
                    // 清除提示信息
                    $(".hint").text("").fadeOut(500);
                    // 创建FormData对象存储数据
                    var formData = new FormData();
                    // 添加二维码内容到表单数据
                    formData.append("codeContent", codeContent);
                    // 如果用户选择了logo文件，则将其添加到表单数据
                    if (logoFile) {
     
     
                        formData.append("logoFile", logoFile);
                    }
                    // 发送AJAX请求
                    $.ajax({
     
     
                        // 请求URL
                        url: "/qrCode",
                        // 请求类型
                        type: "POST",
                        // 请求数据
                        data: formData,
                        // 不对数据进行序列化处理
                        processData: false,
                        // 不设置content-type头
                        contentType: false,
                        // 成功回调
                        success: function (data) {
     
     
                            // 检查返回的数据是否符合base64图片格式
                            if (/^data:image\/png;base64,[A-Za-z0-9+/]{42,}={0,2}$/.test(data)) {
     
     
                                console.log('Received valid base64 data:', data);
                                // 获取画布元素
                                var canvas = document.getElementById('qrCanvas');
                                // 获取画布上下文
                                var ctx = canvas.getContext('2d'
```