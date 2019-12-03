**定义方法的功能**

* 方法用于封装一个特定的功能
* 定义方法的五个要素： 修饰词、返回值类型、方法名、参数列表、方法体；

![1568528399774](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528399774.png)

**return语句**

* 可通过return语句返回，return语句的作用在于结束方法且将数据返回给调用方

![1568528504008](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528504008.png)

**调用方法时的参数传递**

```java
public static int max(int a,int b){......}
int a = 5;
int b = 6;
int myMax = max(a,b);
```

![1568528810136](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528810136.png)

![1568528822096](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528822096.png)

![1568528836840](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528836840.png)

![1568528849615](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528849615.png)

![1568528862408](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568528862408.png)

**写GuassChar中需要注意的部分**

* 有个Arrays类中的函数，Arrays.toString(arr)，很好用，把字符数组转化成字符串
* 新建scanner对象的时候，别忘了System.in
* 把字符串转化成字符数组，可以用 .toCharArray()来做。
* 大写字母的Unicode码是65到90

