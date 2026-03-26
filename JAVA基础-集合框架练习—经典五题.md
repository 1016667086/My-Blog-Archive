### 1.如何将集合中的两个元素交换位置？

```
package File;

import java.util.ArrayList;
import java.util.List;

public class ChangeArraylistPosition {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        list.add("d");
        list.add("e");
        list.add("f");
        swap(list,1,3);
        System.out.println(list);
    }
    /*
    将集合中的两个元素交换位置；
    1.void
    2.List list,int index1,int index2
     */
    public static void swap(List<String>list,int index1,int index2){
        String temp = list.get(index1);     // a,定义一个临时变量，记住其中一个元素。
        list.set(index1,list.get(index2));  // b,用第一个位置存放第二个位置上的元素。
        list.set(index2,temp);              // c.用第二个位置存放临时变量记住的元素。
    }
}


```

运行结果：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/9c8148b8f236b20093c98ab9666f1bb8.png)

### 2.在集合中存储多个Person对象，Person有姓名和年龄，找出年龄最大的那个人。

Person类：

```
package File;

public class Person {
    private  String name;
    private  int age;

    public Person() {
        super();
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}


```

集合类ChangeArraylistPosition：

```
package File;

import java.util.ArrayList;
import java.util.List;

public class OldPerson {

    public static void main(String[] args) {
        ArrayList<Person> list = new ArrayList<>();
        list.add(new Person("张三", 30));
        list.add(new Person("李四", 10));
        list.add(new Person("王五", 40));
        list.add(new Person("赵六", 20));
        list.add(new Person("海海", 60));
        list.add(new Person("妞妞", 38));
        System.out.println("年龄最大的是："+getOldPerson(list));
    }
    /**
     * 获取集合中最老的人
     * 1.Person
     * 2.List<person> list
     */
    public static Person getOldPerson(List<Person> list) {
        Person old = list.get(0);                        //1.定义一个Person类型的变量，先记住第一个元素。
        for (int i = 1; i < list.size(); i++) {          //2.循环遍历集合。
            if (old.getAge() < list.get(i).getAge()) {   //3.用每一个元素和变量年龄，如果集合中的元素比变量记住的年龄大。
                old = list.get(i);                       //4.用变量记住这个年林较大的元素。
            }
        }
        return old;                                      //5.最后将这个年龄返回出去。
    }
}


```

运行结果：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d95c3fed27d62c9190a1ebee6354b775.png)

### 3.把集合的元素反转

```
package File;

import java.util.ArrayList;
import java.util.List;

public class Rev {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
        list.add("d");
        list.add("e");
        list.add("f");
        System.out.println(list);
        System.out.println("反转后：");
        revList(list);
        System.out.println(list);
    }
    /**
     * 将集合中的元素反转
     * 返回值无：void
     * list<E>
     */
    public static <E> void revList(List<E> list){
        for (int i = 0; i < list.size()/2; i++) {
            E temp  = list.get(i);
            list.set(i,list.get(list.size()-1-i));
            list.set(list.size()-1-i,temp);
        }
    }
}


```

运行结果：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/3f630f1a2695d10e6b47dc302894fd92.png)

### 4.获取字符串在集合中出现的次数。

```
package File;

import java.util.ArrayList;
import java.util.List;


public class Count {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("a");
        list.add("a");
        list.add("a");
        list.add("b");
        list.add("b");
        list.add("c");
        list.add("d");
        list.add("d");
        list.add("d");
        list.add("d");
        list.add("d");
        System.out.println("a出现的次数："+frequency(list,"a"));
        System.out.println("b出现的次数："+frequency(list,"b"));
        System.out.println("c出现的次数："+frequency(list,"c"));
        System.out.println("d出现的次数："+frequency(list,"d"));
        System.out.println("e出现的次数："+frequency(list,"e"));
    }

    private static int frequency(List<String> list, String a) {
        int count = 0;                          //定义计数器，开始归0
        for (String string: list) {             //遍历集合
            if (a.equals(string)) {             //判断传入的字符串和已有的字符串是否相等
                count++;                        //如果相等计数器+1
            }
        }
        return count;                           //返回计数器。
    }
}


```

运行结果：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/932e7cb839c5da35c037e7c82bd6a753.png)

### 5.定义一个replaceAll方法，将传入的新值替换集合中的老值。

```
package File;

import java.util.ArrayList;
import java.util.List;

public class ReplaceAll {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("a");
        list.add("a");
        list.add("a");
        list.add("b");
        list.add("b");
        list.add("c");
        list.add("d");
        list.add("d");
        list.add("d");
        list.add("d");
        list.add("d");
        System.out.println("换前：" + list);
        replaceAll(list, "a", "z");
        System.out.println("替换后" + list);
    }
    /**
     * 提花集合中的元素
     * 返回值 void
     * 参数：List<String> list,String oldStr,String newStR</>
     */
    public static void replaceAll(List<String> list, String oldStr, String newStr) {
        for (int i = 0; i < list.size(); i++) {            //遍历集合。
            if (oldStr.equals(list.get(i))) {              //如果传入的老元素与集合中的元素相等。
                list.set(i, newStr);                        //就把这个元素换成新传入的元素。
            }
        }
    }
}

}


```

运行结果：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/fca822c101949533f2ffb9b607722bec.png)