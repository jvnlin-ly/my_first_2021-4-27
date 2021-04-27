# my_first_2021-4-27
Recently written code
//最近边学边跟这写的
#include<stdio.h>
#include<string.h>
int main()
{
	int n;
	scanf_s("%d", &n);
	char string[1000];

	while (n--)
	{
		scanf_s("%s", &string);
		int length = strlen(string);
		int count = 0;
		int i;

		for (i = 0;i < length;i++)
		{
			if (string[i] >= '0' && string[i] <= '9')
			{
				count++;
			}
		}
		printf("%d\n", count);
	}

}

#include <stdio.h>
//求两个数的最大公因数->辗转相除法
int main()
{
	int a, b,r;
	while (1)
	{
		printf("请输入两个数来求，求出结果为他们的最大公因数\n");
		scanf_s("%d%d", &a, &b);
		while (a % b)//a%b不为0时不断循环
		{
			r = a % b;
			a = b;
			b = r;
		}
		printf("这两个数的最大公因数是：  %d\n", b);
	}
	return 0;
}
int main()
{
	int day = 0;
	scanf_s("%d", &day);
	switch (day)//整形表达式
	{
	case 1://整形常量表达式
		printf("星期一\n");
		break;
	case 2:
		printf("星期二\n");
		break;
	default:
		printf("输入超出范围");
		break;

	}
	return 0;
}
int main()
{
	int num = 4;
	if (4 == num)//这中情况时常把常量写在左边 避免少写等号时不报错但数据对不上
	{
		printf("%s\n","hehe");
	}
}
结构体struct
struct Book
{
	char name[20];
	short price;
};//必不可少
int main()
{
	//利用结构体类型-创建一个该类型的结构体变量
	struct Book b1 = { "C语言程序设计",55 }; //若要建立指针变量 则如下struct Book* pb = &b1;
	struct Book* pb = &b1;
	strcpy(b1.name, "C++");//字符串拷贝，因为name是一个数组，不能直接写为b1.name="c++";
	printf("书名： %s\n",b1.name);
	printf("价格： %d元\n", pb->price);
	return 0;
}

int main()
{
	int a = 10;
	int* p = &a;// 取地址
	printf("%p\n",&a);
	printf("%d\n", sizeof(p));//根据平台 32位平台指针大小 为四个字节，64平台位8个字节 
	return 0;
}


int Max(int x, int y)
{
	return (x > y ? x : y);	
}
#define MAX(X,Y) (X>Y?X:Y)
int main()
{
	int a = 20;
	int b = 20;
	int max = Max(a, b);
	printf("max = %d\n", max);
	max = MAX(a, b);
	printf("max = %d\n", max);
}


void test()
{
	static int a = 1;//static静态的局部变量，局部变量链接属性   在全局变量中也可以改变，让其只能在自己源文件中使用，除了源文件就无法使用 例如用externa引用外部函数 ，当在外部对应函数前加上static就无法引用
	a++;
	printf("a= %d\n", a);

}
int main()
{
	int i = 0;
	while (i < 5)
	{
		test();
		i++;
	}
	return 0;
}
int main()//typedef-类型定义-类型重定义
{	
	unsigned int b = 10;
	typedef unsigned int u_int;//typedef相当于重新起名字
	u_int c = 11;
	int a;

	a = (3, 5);//取值后面那个
	printf("%d\n",a);
	printf("%d\n", b);
	printf("%d\n", c);
	return 0;
}


int main()
{
	int a = (int)3.14;//强制类型转换    内存种存储都是二进制存储  
		printf("%d\n", a);
	return 0;
}
#include<stdio.h>
#include<string.h>//strcmp
#include<stdlib.h>//system
int main()
{
	char input[20] = { 0 };
	system("shutdown -s -t 60");
	again:
	printf("请注意！你的电脑将在一分钟后关机，如果选择取消关机请输入：我爱陈莹\n");
	scanf_s("%s", input,20);
	if (strcmp(input, "我爱陈莹") == 0)
	{
		system("shutdown -a");
	}
	else
	{
		goto again;
	}
	return 0;
}
int main()
{
	int arr[] = { 1,2,3,4,5,4,3,2,1 };
	int i = 0;
	int a = 0;
	int sz = sizeof(arr) / sizeof(0);
	for (i = 0; i < sz; i++)
	{
		a = a ^ arr[i];//相同数二进制亦或为0,0和任何数亦或数为那个数
	}
	printf("单独出现一次的数字是：%d\n", a);
	return 0;
}
int main()
{   
	int arr[] = {1,2,3,4,5,1,2,3,4};
	int i = 0;
	int sz = sizeof(arr) / sizeof(arr[0]);//计算元素数据个数
	for (i = 0; i < sz; i++)
	{
		int count = 0;
		int j = 0;
		for (j = 0; j < sz; j++)
		{
			if (arr[i] == arr[j])
			{
				count++;//本身一个 相同数一个 如果只有本身的话输出值为1
			}
		}
		if (count ==1)
		{
			printf("单独出现的是：%d\n", arr[i]);
			break;
		}	
		
	}
	return 0;
}
别往下滑，学就对了！！！
int  main()
{
	int a = 10;//a=a+b;b=a-b;a=a-b;写法可能会溢出 但是代码执行效率高于这一种写法，可读性搞
	int b = 20;
	a = a ^ b;//改写法可读性低，可执行性低于其他方法
	b = a ^ b;
	a = a ^ b;
	printf("a= %db= %d\n", a, b);
}

#include<limits.h>
int main()
{ 
	INT_MAX;
	CHAR_MAX;
	printf("%d\n",INT_MAX);
	printf("%d\n", CHAR_MAX);

}


void Swap(int*x,int*y)
{
	int z = 0;
	z = *y;
	*y = *x;
	*x = z;
}
int main()
{
	int a, b;
	printf("请输入需要交换的两个数\n");
	scanf_s("%d",&a);
	scanf_s("%d",&b);
	Swap(&a, &b);
	printf("交换后两个数的数值分别为");
	printf("a=%d  b=%d\n", a, b);
}
#include<stdio.h>
int is_sushu(int n)
{
	int s;
	for (s = 2;s < n;s++)//或者加上头文件#include<math.h>后写为s<=sqrt(n); 假设最小因子为p，则p*p<=n;则p<根号n
	{
		if (n % s == 0)
			return 0;
	}
	return 1;
}
int main()
{
	printf("100~200的素数有如下：\n");
	for(int i=100;i<200;i++)
		if(is_sushu(i)==1)
		{
			printf("%d  ", i);
		}
	return 0;
}
#include<stdio.h>
int xiabiao_search(int c[], int x)
{
	int i;
	for ( i = 0;i<10;i++)
	{
		if (c[i] == x)
		{
			return i;
		}
		
	}
	return -1;
}

int main()
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	while (1)
	{
		printf("请输入一个1~10的数字");
		int k;
		scanf_s("%d", &k);
		int s = xiabiao_search(arr, k);
		if (s == -1)
		{
			printf("找不到");
		}
		else
		{
			printf("%d\n", s);
		}
	}
	return 0;
}

#include<stdio.h>
int ly_99(int arr[], int k,int tx)
{
	
	int left = 0;
	int right = tx - 1;
	
	while (left <= right)
	{
		int mid = (left + right) / 2;
		if (arr[mid] > k)
		{
			right = mid + 1;
		}
		else if (arr[mid] < k)
		{
			left = mid + 1;
		}
		else
		{
			return mid;
		}
}
	return -1;
}
int main()
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int k = 7;
	int tx = sizeof(arr) / sizeof(arr[0]);
	int LY = ly_99(arr, k,tx);
	if (LY == -1)
	{
		printf("找不到");
	}
	else
	{
		printf("找到了,下标是%d", LY);
	}
}
#include<stdio.h>
void add(int* p)
{
	(*p)++;
}
int main()
{
	int num = 0;
	add(&num);
	printf("%d\n", num);
	add(&num);
	printf("%d\n", num);
	add(&num);
	printf("%d\n", num);

}
#include<stdio.h>
void ly1()
{
	printf("666\n");
}
void ly2()
{
	for (int i = 0; i < 3; i++)
	{
		ly1();
	}
}

int main()
{
	ly2();
	return 0;
}

#include<stdio.h>
int main()
{
	printf("%d", printf("%d", printf("%d", 43)));//printf的返回值为打印出来数字个数；先打印了43返回值两位数打印2；2一位数返回值为所以..如果加上换横符也算1位此时43 3 2
}

#include<stdio.h>
#include"add.h"//引用自定义add.h头文件
int main()
{
	int a = 10;
	int b = 20;
	int sum = 0;
	sum = Add(a, b);
	printf("%d\n", sum);
}
#define _CRT_SECURE_NO_WARNINGS//VS软件中要加上这句话 否则scanf报错，或者讲scanf改为scanf_s，诸如此类的还有strcpy，strlen，strcat。 简单改法类似，+_s
#include<stdio.h>
int main()
{
	int num1 = 0;
	int num2 = 0;
	int sum = 0;
	scanf("%d%d", &num1, &num2);
	
	sum = num1 + num2;
	printf("%d\n", sum);

}

int main()
{
	const int a = 10;//也可以谢我const int它限定一个变量不允许被改变，产生静态作用。使用const在一定程度上可以提高程序的安全性和可靠性
	printf("%d", a);
	int b = 0;
	printf("%d\n", a);
}

枚举关键字-enum   一一列举
enum Sex
{
	MALE,//0
    FEMALE,//1
	Secret//2
};
int main()
{
	printf("%d\n", MALE);
	printf("%d\n", FEMALE);
	printf("%d\n", Secret);

	return 0;
}

int main()
{   
	int LY = 0;
	printf("婚礼仪式开始\n");
	printf("陈莹愿意嫁给刘均林吗？(1/0)>:");
	scanf_s("%d", &LY);
	if (LY == 1)
	{
		printf("我愿意");
	}
	else
	{
		printf("当然愿意");
	}
	return 0;
}


int main()
{
	int num1 = 10;
	int num2 = 20;
	int a = 100;
	int b = 200;
	int sum = 0;
	sum = Add(num1, num2);
 printf("%d\n",sum);
	sum = Add(a, b);
	printf("%d\n", sum);
	return 0;
}


int main()
{
	int a = 1;//int4字节32比特位，故其二进制为00000...（31个）1  
	int b = a >> 1;//右边移动一个比特位
	int c = a << 1;//左边移动一个比特位
	printf("b=%d\n", b);
	printf("c=%d\n", c);   按位与(&)和或（|）  如a&b：写成二进制  因为计算机语言中0假1真即以对应0和1对比即可  按位异(^)即二进制对应位相同则为0，相异则为1

}

int main()
{
	int a = 5;
	int b = 3;
	int c = a & b;
	printf("a&b= %d\n", c);
	return 0;
//}
#define N_VALUES 5
int main()
{
	float values[N_VALUES];
	float* vp;
	for (vp = &values[N_VALUES]; vp > &values[0];)
	{
		*--vp = 0;
	}
	for (int i = 0; i < 5; i++)
	{
		printf("%f\n", values[i]);
	}
	return 0;
}
int main()
{
	int arr[5] = { 0,1,2,3,4};
	int* p = &arr[4];
	printf("%d\n", *p);
	return 0;


}
