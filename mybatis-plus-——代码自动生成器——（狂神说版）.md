#### 文章目录

* [前言](#_7)
* [使用步骤](#_14)
* [写在最后](#_123)

---

## 前言

代码生成器不是一个exe的执行文件，他是通过编写一个类并执行该类的程序代码，通过执行代码的方式让程序自动编写`dao、pojo、service、controller`…代码，其中`AutoGenerator` 是 `MyBatis-Plus` 的代码生成器，通过 `AutoGenerator` 可以快速生成 `Entity`、  
 `Mapper`、`Mapper XML`、`Service`、`Controller` 等各个模块的代码，从而极大的提升了开发效率。

## 使用步骤

其中 `String projectPath = System.getProperty("user.dir");`表示user下的文件夹，通过全局配置把自动生成的代码放到我们指定的文件夹下`gc.setOutputDir(projectPath + "/src/main/java");`

还有设置数据源 代码中

```
dsc.setUrl(
        "jdbc:mysql://localhost:3306/mybatis_plus?"
            + "useSSL=false&useUnicode=true&characterEncoding=utf-8&serverTimezone=GMT%2B8");
            + 

```

需要设置自己mysql中数据库的名字以及数据库ip与端口号。

最后呢就是设置文件生成对应的包下：`pc.setParent("com.kuang");`

配置乐观锁：

```
 // 乐观锁
    strategy.setVersionFieldName("version");
    strategy.setRestControllerStyle(true);
    strategy.setControllerMappingHyphenStyle(true);

```

源代码如下：

```
package com.kuang;
import com.baomidou.mybatisplus.annotation.DbType;
import com.baomidou.mybatisplus.annotation.FieldFill;
import com.baomidou.mybatisplus.annotation.IdType;
import com.baomidou.mybatisplus.annotation.TableField;
import com.baomidou.mybatisplus.generator.AutoGenerator;
import com.baomidou.mybatisplus.generator.config.DataSourceConfig;
import com.baomidou.mybatisplus.generator.config.GlobalConfig;
import com.baomidou.mybatisplus.generator.config.PackageConfig;
import com.baomidou.mybatisplus.generator.config.StrategyConfig;
import com.baomidou.mybatisplus.generator.config.po.TableFill;
import com.baomidou.mybatisplus.generator.config.rules.DateType;
import com.baomidou.mybatisplus.generator.config.rules.NamingStrategy;
import java.util.ArrayList;
// 代码自动生成器
public class KuangCode {
  public static void main(String[] args) {
    // 需要构建一个 代码自动生成器 对象
    AutoGenerator mpg = new AutoGenerator();
    // 配置策略
    // 1、全局配置
    GlobalConfig gc = new GlobalConfig();
    String projectPath = System.getProperty("user.dir");
    gc.setOutputDir(projectPath+"/src/main/java");
    gc.setAuthor("狂神说");
    gc.setOpen(false);
    gc.setFileOverride(false); // 是否覆盖
    gc.setServiceName("%sService"); // 去Service的I前缀
    gc.setIdType(IdType.ID_WORKER);
    gc.setDateType(DateType.ONLY_DATE);
    gc.setSwagger2(true);
    mpg.setGlobalConfig(gc);
    //2、设置数据源
    DataSourceConfig dsc = new DataSourceConfig();
    dsc.setUrl("jdbc:mysql://localhost:3306/kuang_community?
useSSL=false&useUnicode=true&characterEncoding=utf-8&serverTimezone=GMT%2B8");
    dsc.setDriverName("com.mysql.cj.jdbc.Driver");
    dsc.setUsername("root");
    dsc.setPassword("123456");
    dsc.setDbType(DbType.MYSQL);
    mpg.setDataSource(dsc);
    //3、包的配置
    PackageConfig pc = new PackageConfig();
    pc.setModuleName("blog");
    pc.setParent("com.kuang");
    pc.setEntity("entity");
    pc.setMapper("mapper");
    pc.setService("service");
    pc.setController("controller");
    mpg.setPackageInfo(pc);
    //4、策略配置
    StrategyConfig strategy = new StrategyConfig();
  
 strategy.setInclude("blog_tags","course","links","sys_settings","user_record","
user_say"); // 设置要映射的表名
    strategy.setNaming(NamingStrategy.underline_to_camel);
    strategy.setColumnNaming(NamingStrategy.underline_to_camel);
    strategy.setEntityLombokModel(true); // 自动lombok；
    strategy.setLogicDeleteFieldName("deleted");
    // 自动填充配置
    TableFill gmtCreate = new TableFill("gmt_create", FieldFill.INSERT);
    TableFill gmtModified = new TableFill("gmt_modified",
FieldFill.INSERT_UPDATE);
    ArrayList<TableFill> tableFills = new ArrayList<>();
    tableFills.add(gmtCreate);
    tableFills.add(gmtModified);
    strategy.setTableFillList(tableFills);
    // 乐观锁
    strategy.setVersionFieldName("version");
    strategy.setRestControllerStyle(true);
    strategy.setControllerMappingHyphenStyle(true); //
localhost:8080/hello_id_2
    mpg.setStrategy(strategy);
    mpg.execute(); //执行
 }
}

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/4fe427b5b86153b48382ffd96bf16960.png)

## 写在最后

> 人到了一定年龄，一定要懂得把心情和脾气调成静音模式，然后不动声色的打理自己，过好余生的每一天。