@[TOC]
# 一、类的表示
类包含 **类名、属性、方法**
采用带有双分割线的矩形表示，如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/ed82188952af4842a478e6ea6ffd1639.png)


*\[ ]:表示可选*

1、类名：```使用非斜体(正体)表示```
2、属性：`修饰符(可见性) 属性名:类型[=默认值]`
3、方法：```修饰符(可见性) 方法名(参数列表)[:返回值类型]```

 **修饰符(可见性)：**
- +:public
- -:private
- #:protected
-  :default     	 ***注意:这里啥也不加表示默认***

![在这里插入图片描述](https://img-blog.csdnimg.cn/cc131dc2f3fd46179e64fa52532d21c6.png)
# 二、类与类之间的表示方式
## 1、关联关系
关联关系表示 一个类中使用了另一个类的对象
使用实现箭头表示
![在这里插入图片描述](https://img-blog.csdnimg.cn/b69029b305954e0dbe2b400dcf99d2bc.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/e16ac770e2db4e619dd739267b05b41c.png)


表示 Teacher类中有一个Student类对象
![在这里插入图片描述](https://img-blog.csdnimg.cn/e56245feff8d40f992e58e3e2062fd18.png)

## 2、聚合关系
**强关联关系**。
**整体和部分的关系**。
**整体不存在了，部分依然存在**
*例如 一个大学有很多的老师*
![在这里插入图片描述](https://img-blog.csdnimg.cn/38331246256744618b42470d93da6afa.png)



使用带空心的菱形直线表示。空心菱形指向整体。
![在这里插入图片描述](https://img-blog.csdnimg.cn/aa3c225766c64c3abdcac20103f00b7e.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBATWFlX3N0cml2ZQ==,size_20,color_FFFFFF,t_70,g_se,x_16)

## 3、组合关系
**更强烈的关联关系**
与聚合关系不同的是，**整体不存在了，部分也将不存在**。
*例如 一个国家有很多的人*
使用带实心的菱形直线表示。实心菱形指向整体。
![在这里插入图片描述](https://img-blog.csdnimg.cn/80879c1d25d643f19d8051cfdff2c26f.png)


![!\[在这里插入图片描述\](https://img-blog.csdnimg.cn/5c20ccfb5c4347f](https://img-blog.csdnimg.cn/e9353626d3cf43e199ca7dc6accb1ee9.png)
1b052502bf42ec152.png)
## 4、依赖关系
是一种**使用关系**。
即某个类通过 **局部变量、方法参数、静态方法**的调用访问另一个类中的某些方法。
使用带箭头的虚线表示，箭头指向被调用(被依赖)类。
![在这里插入图片描述](https://img-blog.csdnimg.cn/fc40c81c733146d78fb39de737c2f63f.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/050b7da659284314855245a7e62bd548.png)
# 三、接口的表示
接口包含**接口名、接口方法**
使用带单横线的矩形表示
1、接口名上面带有<\<interface>>
2、接口方法：```修饰符(可见性) 方法名(参数列表)[:返回值类型]```
![在这里插入图片描述](https://img-blog.csdnimg.cn/e150355faca349f3bf6cbe17be51c96a.png)
# 四、抽象类的表示
抽象类包含 **类名、属性、方法**
采用带有双分割线的矩形表示。

1、类名：```使用斜体表示```
2、属性：`修饰符(可见性) 属性名:类型[=默认值]`
3、方法：```修饰符(可见性) 方法名(参数列表)[:返回值类型]```
![在这里插入图片描述](https://img-blog.csdnimg.cn/22e2ff49372f44bda71cf6d1c0df9fab.png)
# 五、类与接口、抽象类之间的关系
## 1、继承关系
使用**空心三角形实线**表示，空心三角形指向被继承类.
![在这里插入图片描述](https://img-blog.csdnimg.cn/5bc4d6ffb4a24470861c94c83609ccfb.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/d03979d8967b4a119affc95e474f2b6d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBATWFlX3N0cml2ZQ==,size_10,color_FFFFFF,t_70,g_se,x_16)

## 2、实现关系
使用**空心三角形虚线**表示，空心三角形指向被实现接口.
![在这里插入图片描述](https://img-blog.csdnimg.cn/dd334c77d23249c4b9c56ed4d7205d55.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/d88ff04d66044492896719a5f33f65f3.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBATWFlX3N0cml2ZQ==,size_11,color_FFFFFF,t_70,g_se,x_16)
