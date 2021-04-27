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
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
//int main()
//{
//	char a [10]= "111";
//	strcat(a, "333");
//	printf("%s\n", a);
//	strcpy(a, "333");
//	printf("%s\n", a);
//	return 0;
//}
//struct book
//{
//	char name[20];
//	short price;
//};
//
//int main()
//{
//	struct book b1 = { "C语言程序设计" };
//	strcpy(b1.name, "C++");
//	printf("%s\n", b1.name);
//	return 0;
//
//
//}
//int main()
//{
//	int a = 10;
//	int b = 5;
//	printf("%d\n", (a > b ? a : b));
//	return 0;
//}
//struct student
//{
//	char name[20];
//	int age;
//	char ID[20];
//};
//int main()
//{
//	int a = 10;
//	struct student l = { "刘",20,"3202070820413" };
//	printf("姓名： %s\n年龄： %d\n学号： %s\n", l.name,l.age,l.ID);
//	printf("年龄： %d\n", l.age);
//	struct student* ps = &l;
//	printf("姓名：%s\n", (*ps).name);
//	printf("年龄：%d\n", ps->age);
//	return 0;
//}
//int main()
//{
//	char a = 3;
//	//00000000000000000000000000000011
//	//00000011 会发生截断 故此时a=00000011
//	char b = 127;
//	//00000000000000000000000001111111
//	//01111111截断 因为char类型一个字节
//	char c = a + b;
//	//00000011
//    //01111111
//	//相加时候 前面补零   若为负数补1
//	//00000000000000000000000000000011
//	//00000000000000000000000001111111
//	//00000000000000000000000010000010
//
//	//c 10000010
//	//11111111111111111111111110000010-->补码
//	//11111111111111111111111110000001-->反码
//	//10000000000000000000000001111110-->原码
//	//打印的是原码:
//	printf("%d\n", c);
//
//	return 0;
//}
//int main()
//{
//    char a=1;
//	printf("%d\n", sizeof(a));
//	printf("%d\n", sizeof(+a));//a被转化为整形故为4字节
//	printf("%d\n", sizeof(!a));
//	return 0;
//}
//int main()
//{
//	
//	return 0;
//}

//int main()
//{
//	int a = 10;
//	int* pa = &a;
//	int** paa = &pa;
//	printf("%d", **paa);
//	return 0;
//}

//void Printf(int arr[], int sz)
//{
//	int i = 0;
//	{
//		for (i = 0; i < sz; i++)
//		{
//			printf("%d ", arr[i]);
//		}
//		printf("\n");
//	}
//}
//void reverse(int arr[],int sz)
//{
//	int left = 0;
//	int right = sz - 1;
//	int temp;
//	while (left < right)
//	{
//		temp = arr[right];
//		arr[right]=arr[left];
//		arr[left] = temp;
//		left++;
//		right--;
//	}
//}
//int main()
//{
//	int arr[10] = { 1,2,3,4,5,6,7,8,9,10 };
//	int sz = sizeof(arr) / sizeof(arr[1]);
//	Printf(arr, sz);
//	reverse(arr, sz);
//	Printf(arr, sz);
//	return 0;
//}

//void print(int arr1[], int arr2[], int sz)
//{
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d ", arr1[i]);
//	}
//	printf("\n");
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d ", arr2[i]);
//	}
//	printf("\n");
//}
//void exchange(int arr1[], int arr2[], int sz)
//{
//	int i = 0;
//	int temp;
//	for (i = 0; i < sz; i++)
//	{
//		temp = arr1[i];
//		arr1[i] = arr2[i];
//		arr2[i] = temp;
//	}
//}
//int main()
//{
//	int arr1[5] = { 1,2,3,4,5 };
//	int arr2[5] = { 6,7,8,9,10 };
//	int sz = sizeof(arr1) / sizeof(arr1[1]);
//	printf("交换两数组前粉别的数组值\n");
//	print(arr1,arr2, sz);
//	exchange(arr1, arr2, sz);
//	printf("交换两数组后粉别的数组值\n");
//	print(arr1, arr2, sz);
//	return 0;
//}
//测试二进制的1的数字数

//int coubt_bit_one(int a)//此写法更好于下面写法
//{
//	int count = 0;
//	//for(int i=0;i<32;i++)
//	//{
//	//	if ( (a>>i)&1==1)
//	//	{
//	//		count++;  
//	//	}
//	//}
// //或者写为
// while(a)
// {
//  a=a&(a-1);
// count++;
// }
//return count;
//}
//int coubt_bit_one(unsigned int a)//解决无符号数的问题
//{
//	int count = 0;
//	while (a)
//	{
//		if (a % 2==1)
//		{
//			count++;
//		}
//		a = a / 2;
//
//	}
//	return count;
//}
//int main()
//{
//	int a;
//	scanf("%d", &a);
//	//写一个函数求a二进制（补码）表示有多少个1
//	int count =coubt_bit_one(a);
//	printf("%d", count);
//	return 0;
//}

//求两个32位的二进制数字的对应数字数相同个数
//int get(int a, int b)
//{
//	int count = 0;
//	int temp = a ^ b;//将相同数字转化为1  按照上求1个数来求相同数字个数
//	while (temp)
//	{
//		temp = temp&(temp-1);
//		count++;
//	}
//	return count;
//}
//int main()
//{
//	int a, b;
//	scanf("%d%d", &a,& b);
//	int count=get(a,b);
//	printf("%d\n",count);
//	return 0;
//}
//void print(int m)
//{
//	int i = 0;
//	printf("打印奇数位");
//	for (i = 30; i >= 0; i -= 2)
//	{
//		printf("%d ", (m >> i) & 1);// 打印奇数位   二进制
//	}
//	printf("\n");
//	printf("打印偶数位");
//
//	for (i = 31; i >=1; i -= 2)
//	{
//		printf("%d ", (m >> i) & 1);
//	}
//}
//int main()
//{
//	int m = 0;
//	scanf("%d", &m);
//	print(m);
//	return 0;
//}

//void print(int* p, int sz)
//{
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d ",*(p + i));
//	}
//}
//int main()
//{
//	int arr[] = {1,2,3,4,5,6,7,8,9 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	print(arr, sz);
//	return 0;
//
//
//}

//void print(int n)
//{
//	int i = 0;
//	int j = 0;
//	for (i = 1; i <= n; i++)
//	{
//		for (j = 1; j <= i; j++)
//		{
//			printf("%d*%d=%-4d ", i, j, i * j);
//		}
//		printf("\n");
//	}
//}
//int main()
//{
//	int n ;
//	scanf("%d", &n);
//	print(n);
//	return 0;
//}
//int my_strlen(char* str)
//{
//	int count = 0;
//	while (*str != '\0')
//	{
//		count++;
//		str++;
//	}
//	return count;
//}
//void reverse_string(char str[])
//{
//	int left = 0;
//	int right =my_strlen(str)-1;
//	char stem;
//	while(left<right)
//	{
//		stem = str[right];
//		str[right] = str[left];
//		str[left] = stem;
//		left++;
//		right--;
//	}
//}
//int main()
//{
//	char str[] = "abcd";
//	//int sz = sizeof(str) / sizeof(str[1]);
//	reverse_string(str);
//	printf("%s\n", str);
//	return 0;
//}
//
//void reverse_string(char str[],int sz)
//{
//	int left = 0;
//	int right =sz-2;
//	char stem;
//	while(left<right)
//	{
//		stem = str[right];
//		str[right] = str[left];
//		str[left] = stem;
//		left++;
//		right--;
//	}
//}
//int main()
//{
//	char str[] = "abcd";
//	int sz = sizeof(str) / sizeof(str[1]);
//	reverse_string(str,sz);
//	printf("%s\n", str);
//	return 0;
//}

//
//void reverse_string(char* str)
//{
//	char tmp = str[0];
//	int len = my_strlen(str);
//		str[0] = str[len - 1];
//		str[len - 1] = '\0';
//		if (my_strlen(str+1)>=2)
//		{
//			reverse_string(str + 1);
//		}
//		str[len - 1] = tmp;//最后位置放a
//}
//int main()
//{
//	char str[] = "abcd";
//	reverse_string(str);
//	printf("%s\n", str);
//	return 0;
//}

//int Digitsum(int a)
//{
//	if (a > 9)
//	{
//		return Digitsum(a / 10) + a % 10;
//	}
//	else
//	{
//		return a;
//	}
//}
//int main()
//{
//	unsigned int a;
//	scanf("%d", &a);
//	int ret = Digitsum(a);
//	printf("%d\n", ret);
//	return 0;
//}
//double pow(int n,int k)
//{
//	if (k < 0)
//	{
//		return(1.0 /pow(n,-k));//k转化为正数 调用函数 在倒数
//	}
//	else if (k == 0)
//	{
//		return 1;
//	}
//	else
//	{
//		return n* pow(n, k - 1);
//	}
//}
//int main()
//{
//	int n = 0;
//	int k = 0;
//	scanf("%d%d",&n,&k);
//	double ret = pow(n,k);
//	printf("ret = %lf", ret);
//	return 0;
//}

//描述一个学生  - - 数据
//
//struct stu
//{
//	char name[20];
//	short age;
//	char tele[20];
//	char sex[5];
//
//}s1, s2, s3;	//s1 s2 s3三个全局结构体变量  
//typedef struct stu//typedef将其命名为stu 两个名字皆可以使用
//{
//	char name[20];
//	short age;
//	char tele[20];
//	char sex[5];
//
//}stu;
//int main()
//{
//	struct stu s = {"小刘",20,"19127812963","男"};//s为局部结构体变量
//	stu s2;
//	return 0;
//}

//struct s
//{
//	int a;
//	char c[20];
//};
//struct t
//{
//	char ch[10];
//	struct s y;
//	char* p;
//};
//int main()
//{
//	char arr[] = "hello";
//	struct t l ={ "小黑", {20,"hello word"},arr };
//	printf("%d\n",l.y.a);
//	printf("%s\n", l.y.c);
//	printf("%s\n", l.p);
//	return 0;
//}
//
//typedef struct stu//typedef将其命名为stu 两个名字皆可以使用
//{
//	char name[20];
//	short age;
//	char tele[20];
//	char sex[5];
//
//}stu;
//void print1(stu tmp)
//{
//	printf("name:%s\n", tmp.name);
//
//}
//void print2(stu* l)
//{
//	printf("sex: %s\n", l->sex);
//}
//int main()
//{
//	stu s = {"李四",40,"168816666","公"};
//	print1(s);//函数传参需要压栈 
//	print2(&s);//传地址 只需要创建指针变量的空间  优选print2;
// 	return 0;
//}
//
//
//int main()//把奇数放前面 偶数放后面
//{
//	int money = 0;
//	int total = 0;
//	int empty = 0;
//	scanf("%d", &money);
//	if (money == 0)
//	{
//		total = 0;
//	}
//	else
//	{
//		total = 2 * money - 1;
//	}
//	//total = money;	 
//	//empty = money;
//	//while (empty >= 2)
//	//{
//	//	total+=empty /2;
//	//	empty = empty / 2 + empty % 2;
//	//}
//	printf("总共：%d\n", total);
//	return 0;
//}
//void print(int*p, int sz)
//{
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d,",p[i]);
//	}
//	printf("\n");
//}
//void move(int* a,int sz)//从左边找偶数 从右边找奇数
//{
//	int left = 0;
//	int right = sz - 1;
//	//从左边找偶数
//	while (left<right)
//	{
//		while ((left<right)&&a[left] % 2 == 1)//left<right全奇数 时候死循环 
//		{
//			left++;
//		}
//		while ((left < right)&&a[right] % 2 == 0)//left<right  全偶数时候放置死循环
//		{
//			right--;
//		}
//		//右边找奇数
//		if (left < right)
//		{
//			int tmp = a[left];
//			a[left] = a[right];
//			a[right] = tmp;
//		}
//    }
//}
//int main()
//{
//	int arr[] = { 1,2,3,4,5,6,7,8,9 ,10};
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	move(arr,sz);
//	print(arr, sz);
//	return 0;
//}
//杨辉三角
//int main()
//{
//	int arr[10][10] = { 0 };
//	    int i = 0;
//		int j = 0;
//		int k = 0;
//		for (i = 0; i < 10; i++)
//		{
//			for (j = 0; j < 10; j++)
//			{
//				if (j == 0)
//				{
//					arr[i][j] = 1;
//				}
//				if (i == j)
//				{
//					arr[i][j] = 1;
//				}
//				if (i >= 2 && j >= 1)
//				{
//					arr[i][j] = arr[i - 1][j] + arr[i - 1][j - 1];
//				}
//			}
//		}
//		for (i = 0; i < 10; i++)
//		{
//			for (k = 10; k > i; k--)
//			{
//				printf(" ");
//			}
//			for (j = 0; j <=i; j++)
//			{
//				printf("%-4d", arr[i][j]);
//			}
//			printf("\n");
//		}
//	return 0;
//}
//A说不是我
//B说是C
// C说是D
//D说C在胡说   
//已知有一人说假话 三人说真话
//int main()
//{
//	int killer = 0;
//	for (killer = 'a'; killer <= 'd'; killer++)
//	{
//		if ((killer != 'a') + (killer == 'c') + (killer == 'd') + (killer != 'd') == 3)
//		{
//			printf("killer==%c", killer);
//		}
//	}
//	return 0;
//}

//36匹马，6跑道，无计时器，请赛马确定，36匹马前3  求比赛次数  比6次拿各组第一出来比 比出前三 在此次第一的上一场前三 第二拿上一场前二和第三 来 比共八次
//2根材质不均匀香 定15分钟时间段 第一个两边点 第二根点一边  第一根燃完开始点第二根另一端
//A说：B第二，我第三
//B说：我第二，E第四
// C说：我第一，D第二
// D说：C最后，我第三
// E说：我第四，A第一
//结束时候每个人直说了一半 请判断他们的名词
//int main()
//{
//	int a = 0, b = 0, c = 0, e = 0, d = 0;
//	for (a = 1; a <= 5; a++)
//	{
//		for (b = 1; b <= 5; b++)
//		{
//			for (c = 1; c <= 5; c++)
//			{
//				for (d = 1; d <= 5; d++)
//				{
//					for (e = 1; e <= 5; e++)
//					{
//						if (((b==2) + (a==3) == 1) &&
//							((b==2) + (e==4) == 1) &&
//							((c==1) + (d==2) == 1) &&
//							((c==5) + (d==3) == 1) &&
//							((e==4) + (a==1) == 1))
//						{
//							if (a * b * c * d * e == 120)
//							{
//								printf("a=%d\nb=%d\nc=%d\nd=%d\ne=%d\n", a, b, c, d, e);
//							}
//						}
//					}
//				}
//			}
//		}
//	}
//	return 0;
//}
