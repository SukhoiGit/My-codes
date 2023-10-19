/*函数的嵌套调用实例*/
/*题目：使用函数的嵌套调用来求4个数中的最大数*/
/*本例中嵌套调用解析：1.main函数调用max4函数 2.max4函数调用max2函数*/
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>

int max4(int a, int b, int c, int d)
{
	int m;
	m = max2(a, b);
	m = max2(m, c);
	m = max2(m, d);
	return m;
}

int max2(int a, int b)
{
	if (a > b)
		return a;
	else
		return b;
}

int main()
{
	int a, b, c, d, max;
	printf("please input 4 numbers:\n");
	scanf("%d,%d,%d,%d", &a, &b, &c, &d);
	max = max4(a, b, c, d);
	printf("The largest number is %d", max);


	return 0;
}

