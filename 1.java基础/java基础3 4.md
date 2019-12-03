**循环中使用continue语句**

continue 可以跳过循环体中剩余语句而执行下一次循环

```java
int sum = 0;
for(int i=1;i<=100;i++)	//统计总和时，跳过所有个位为3的
{
    if(i%10 ==3)
        continue;
    sum+=i;
}
```



**while和do while**

do while至少执行一次。while最少一次也不执行

```java
//随手写了个课堂作业，不用看
import java.util.Scanner
public class SumV01
{
    public static void main(String[] args)
    {
        System.out.println("将开始10次加法测试");
        int answer = -1;
        int score = 0;
        Scanner input = new Scanner(System.in);
        for(i =1;i<=10;i++)
        {
            int num1 = (int)(Math.random()*100)+1;
            int num2 = (int)(Math.random()*100)+1;
            int result = num1+num2;
            System.out.println("("+i+"). "+num1+"+"+num2+"= ?");
            System.out.println("请输入答案(输入-1退出)：");
            answer = input.nextInt();
            if(answer==-1)
                break;
            else if(answer == result)
            {
                score+=10;
                System.out.println("Correct!");
            }
            else
            {
                System.out.println("Error!");
            }
        }
        System.out.println("此次测验结束，你的分数是："+score);
        input.close();
    }
}
```

```java
import java.util.Scanner
public class Sum02
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner();
        System.out.println("请输入整数（例如10）：");
        int n = scanner.nextInt();
        if(n<=0)
            System.out.println("Error:n>0");
        else if(n ==1)
            System.out.println("1 = 1");
        else
        {
            double result = 1.0;
            String expr = "1";
            for(i=2;i<=n;i++)
            {
                result += 1.0/i;
                expr = expr+"+1/"+i;
            }
            System.out.println(expr+"="+result);
        }
        
    }
}
```

