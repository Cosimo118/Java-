**变量命名**

![1568367857738](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568367857738.png)

java中的变量一定要初始化后才能使用，不然编译错误。(和c++一样，和c不一样)

**java基本类型**

![1568368404267](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568368404267.png)

![1568368481666](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568368481666.png)

**int类型**

除了常用的十进制，十六进制是0x或0X开头，八进制是0开头

**long类型**

如果要表示Long直接量，需要以L或l结尾

```java
long a = 1000000000000;		//编译错误
long b = 1000000000000L;
```

![1568368811258](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568368811258.png)

**通过实践毫秒数来存储日期和实践**

System.currentTimeMills()

![1568368973701](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568368973701.png)

**浮点类型使用常见问题**

* 需要表示float类型的直接量时，需要加“f“或者”F“后缀
* 浮点数存在舍入误差问题

```java
double money = 3.0;
double price = 2.9;
System.out.println(money-price);

//输出结果为0.10000000000000000009（18个0）
//如果要精确的得到0.1应该采用BigDecimal类来实现
```

**类型转化使用常见问题汇总**

1. 强制转化时的精度丧失和溢出
2. 数值运算时的自动转换
3. byte、char、short转换为int的问题

在多种基本类型参与的表达式运算中，运算结果会自动地向较大的类型进行转化，例如

```java
long distance = 10000*365*24*60*60*299792458L;	//正确的
long distance = 10000*365*24*60*60;	//不正确会溢出
long distance = 10000L*365*24*60*60	//正确
```

**byte char short转换为int的问题**

1. int直接量可以直接赋值给byte char 和short，只要不超过其表示范围
2. byte char short三种类型参与运算时，先一律转换成int类型再进行运算

```java
byte b1 = 28;
byte b2 = 20;
byte b3 = b1+b2;	//编译错误，因为b1+b2的结果为int类型
```

