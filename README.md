
36匹马，6跑道，无计时器，请赛马确定，36匹马前3  求比赛次数  比6次拿各组第一出来比 比出前三 在此次第一的上一场前三 第二拿上一场前二和第三 来 比共八次
2根材质不均匀香 定15分钟时间段 第一个两边点 第二根点一边  第一根燃完开始点第二根另一端

A说：B第二，我第三
B说：我第二，E第四
 C说：我第一，D第二
 D说：C最后，我第三
 E说：我第四，A第一
结束时候每个人直说了一半 请判断他们的名词
#include<stdio.h>
int main()
{
	int a = 0, b = 0, c = 0, e = 0, d = 0;
	for (a = 1; a <= 5; a++)
	{
		for (b = 1; b <= 5; b++)
		{
			for (c = 1; c <= 5; c++)
			{
				for (d = 1; d <= 5; d++)
				{
					for (e = 1; e <= 5; e++)
					{
						if (((b==2) + (a==3) == 1) &&
							((b==2) + (e==4) == 1) &&
							((c==1) + (d==2) == 1) &&
							((c==5) + (d==3) == 1) &&
							((e==4) + (a==1) == 1))
						{
							if (a * b * c * d * e == 120)
							{
								printf("a=%d\nb=%d\nc=%d\nd=%d\ne=%d\n", a, b, c, d, e);
							}
						}
					}
				}
			}
		}
	}
	return 0;
}

