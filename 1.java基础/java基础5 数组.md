![1568449608580](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568449608580.png)

![1568449656239](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568449656239.png)

![1568449686086](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568449686086.png)

![1568449890527](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568449890527.png)

![1568449905667](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568449905667.png)



**数组的两种复制方法**

一种是System.arraycopy，有五个参数

![1568450980290](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568450980290.png)

一种是java.util.Arrays类中的copyOf方法

![1568451039818](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568451039818.png)

对数组进行扩容可以用Arrays.copyOf()方法来很轻易地实现

![1568451089081](C:\Users\cxt66\AppData\Roaming\Typora\typora-user-images\1568451089081.png)

```java
import java.util.Random
import java.util.Arrays
public class MaxNumber
{
    public static void main(String[] args)
    {
        int[] arr = new int[10];
        Random ran = new Random();
        for(i = 0;i<arr.length;i++)
        {
            arr[i] = ran.nextInt(100);
        }
        System.out.println("数组中的数据为："+Arrays.toString(arr));
        int max = arr[0];
        for(i = 1;i<arr.length;i++)
        {
            if(arr[i]>max)
                max = arr[i];
        }
        System.out.println("最大值是："+max);
        arr = Arrays.copyof(arr,arr.length+1);
        arr[arr.length-1] = max;
        System.out.println("数组中的数据为："+Arrays.toString(arr));
    }
}
```

```java
//冒泡排序
import java.util.Random;
import java.util.Arrays;
public class BubbleSort
{
    public static void main(String[] args)
    {
        int [] arr = new int[10];
        Random ran = new Random();
        for(int i = 0;i<arr.length;i++)
            arr[i] = ran.nextInt(100);
        int temp = 0;
        for(int i = 0;i<arr.length-1;i++)
        {
            for(int j = arr.length-1;j>i;j--)
            {
                if(arr[j-1]>arr[j])
                {
                    temp = arr[j];
                    arr[j] = arr[j-1];
                    arr[j-1] = temp;
                }
            }
        }
    }
}
```

```java
import java.util.Scanner;
public class helloworld
{
    public static void main(String [] args)
    {
        System.out.println("请输入查找质数的范围：2~");
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        for(int i = 2, n = 0;i<=num;i++)
        {
        	boolean flag = false;
            for(int j =2;j<i;j++)
            {
            	flag = ((i%j)==0);
            	if(flag==true)
            		break;
            }
            if(flag==false)
            {
            	System.out.print(i+" ");
            	n = n+1;
            }
            if(n==10)
            {
            	System.out.println();
            	n = 0;
            }
        }
    }
}
```

```java
int [] arr = {0,1,2,3};
int [] arr = new int[4];
```

```java
import java.util.Arrays
import java.util.Random
public class MinValue
{
    public static void main(String [] args)
    {
        int [] arr = new int[10];
        Random ran = new Random();
        for(int i=0;i<10;i++)
            arr[i] = ran.nextInt(100);
        System.out.println("数组中的元素为："+Arrays.toString(arr));
        int min = 100;
        for(int i = 0;i<10;i++)
            if(arr[i]<min)
                min = arr[i];
        System.out.println("最小值是："+min);
        int [] arr1 = new int[11];
        System.arraycopy(arr,0,arr1,1,10);
        arr1[0] = min;
        System.out.println("新数组中的数据为："+Arrays.toString(arr));
    }
}
```

**这上面的代码大多没经过ide验证，别信**

