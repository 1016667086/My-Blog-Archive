#### 文章目录

* [前言](#_3)
* [一、题目](#_8)
* [二、解题步骤](#_15)
* + [1.创建数据库、表。并为之添加数据。](#1_16)
  + [2.新建查询](#2_27)
* [总结](#_139)

## 前言

       今天老师讲完了MySQL数据库基础，发了一份文档下来，有一些简单的题目布置给我们完成。再次记录一下自己的课后习题，加深印象。

---

## 一、题目

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/49a18c66275a005096ff14eaeb64dff0.png#pic_center)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/e577c370a11ea9591d87b1fc6b4b19e2.png#pic_center)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/7fe8f9c734538ef349607a3a190c337a.png#pic_center)

## 二、解题步骤

### 1.创建数据库、表。并为之添加数据。

咱先依次创建数据库数据表：  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/13d3dfb65c89ca9977e1f2facd5189a4.png#pic_center)

然后为之添加数据：  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/467731a6dbefc4a5769d1d932db281c0.png#pic_center)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/5a2a73ffb1c2fa330df83e609f2ba4f8.png#pic_center)

### 2.新建查询

 查询student表的所有记录语句： 

```
select * from student;

```

查询student表的第2条到4条记录语句：

```
select * from student LIMIT 1,3

```

查询结果：  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/417aa8ac37f0e976487e93d031039c3c.png#pic_center)  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/99b2c35c900ea7fac3869183638668e0.png#pic_center)

查询student表中苏哟有学生的学号、姓名、和院系。

```
select id,Name,department from student;

```

从student表中查询计算机系和英语系的学生信息

```
select * from student
where department = '计算机系' OR department ='英语系';

```

从student表中查询每个院系有多少人;

```
select department,COUNT(*)from student GROUP BY department;

```

从score表中查询每个科目的最高分

```
select c_name, MAX(grade) from score
GROUP BY c_name;

```

查询李四的考试科目（c\_name）和考试成绩（grade）

```

select * from score as s LEFT JOIN 
student as st ON s.stu_id = st.id where name = '李四';

```

用连接的方式查询所有学生的信息和考试信息

```
select * from score as s LEFT JOIN 
student as st ON s.stu_id = st.id;     

```

计算每个学生的总成绩

```
select name,SUM(grade) from score
LEFT JOIN student ON score.stu_id = student.id GROUP BY name; 

```

计算每个考试科目的平均成绩

```
select c_name,AVG(grade) from score GROUP BY c_name;   

```

查询计算机成绩低于95的学生信息

```
select name from score LEFT JOIN student 
ON score.stu_id = student.id GROUP BY c_name HAVING AVG(grade
)<95;

```

查询同时参加计算机和英语考试的学生的信息

```
select name from (select * from score where c_name = '计算机') 
as s inner JOIN (select * from score where c_name = '英语') 
as st on s.stu_id = st.stu_id
 INNER JOIN student on s.stu_id =student.id   

```

将计算机考试成绩按从高到低进行排序

```
select * from score where c_name='计算机' ORDER BY grade DESC; 

```

从student表和score表中查询出学生的学号，然后合并查询结果

```
select * from score as s INNER JOIN student as st ON s.stu_id = st.id;

```

查询姓张或者姓王的同学的姓名、院系和考试科目及成绩

```
select * from score as s INNER JOIN
 student as st ON s.stu_id = st.id where name like '张%' OR
name like '王%'

```

查询都是湖南的学生的姓名、年龄、院系和考试科目及成绩

```
select * from score as s
INNER JOIN student as st ON s.stu_id= st.id where address like '湖南%'

```

---

## 总结

 

1. LIMIT(n,m) 用于分页，后面的参数表示从n开始查m个 ,下标从0开始。
2. In 表示包含那个， in(‘计算机系’,‘英语系’); 只有两个系，限制条件。
3. 查询每个系院有多少人，首先是department 写前面，count(\*)写后面，最后是分组 group by department.
4. 求最高分也同理，科目名字放前面，MAX(grade)放后面， group by c\_name.
5. 当两张表同时有数据需要查询时，用 left join 左连接， 固定写法 `select * from xxx as x left join xxx on xx.id = xxx.id.`
6. 只要查询两张表的信息，就要用到表连接, 其中一张表 用 As 命名 inner join 另外一张表也命名， 通过inner join 于 on 来连接。
7. 排序问题：写在最后面，比如说 order by XXx(表名) desc 是降序，dsc是升序。

> 没有什么事情有象热忱这般具有传染性，它能感动顽石，它是真诚的精髓。

启发于这篇博客，在此基础上完善整理一下。如果本文对你有帮助，请给我一个点赞。

> https://blog.csdn.net/x289231673/article/details/78365941