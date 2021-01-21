# vs2013-1-21
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<string.h>
//int Add(int x, int y)
//{
//	int z = 0;
//	z = x + y;
//	return z;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	scanf("%d %d\n", &a, &b);
//	int sum = Add(a, b);
//	printf("%d\n", sum);
//	return 0;
//}

//int main()
//{
//	char arr1[] = "bit";
//	char arr2[20] = "#########";
//	strcpy(arr2, arr1);
//	printf("%s\n", arr2);
//	//strcpy-string copy-字符串拷贝
//	//strlen-string length-字符串长度有关
//	return 0;
//}

//int main()
//{
//	char str1[] = "Sample string";
//	char str2[40];
//	char str3[40];
//	strcpy(str2, str1);
//	strcpy(str3, "copy successful");
//	printf("str1:%s\nstr2:%s\nstr3:%s\n", str1, str2, str3);
//	return 0;
//}

//memset
//memory-内存 set-设置
//int main()
//{
//	char arr[] = "hello world";
//	memset(arr, '*', 5);
//	printf("%s\n",arr);
//	//***** world
//	return 0;
//}

////函数的定义
////形参-形式参数-形式上的参数
//int get_max(int x, int y)
//{
//	if (x < y)
//		return y;
//	else
//		return x;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	scanf("%d %d", &a, &b);
//	//函数的实现
//	int max=get_max(a, b);
//	printf("%d\n", max);
//	return 0;
//}

//写一个函数可以交换两个整形变量的内容
////不能完成任务
////当实参传给形参的时候
////形参其实是实参的一份临时拷贝
////对形参的修改是不会改变的
//void Swap1(int x, int y)
//{
//	int z = 0;
//	z = x;
//	x = y;
//	y = z;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	scanf("%d %d", &a, &b);
//	Swap(a, b);
//	printf("a=%d b=%d\n", a,b);
//	return 0;
//}//此方法有问题

//int main()
//{
//	int a = 10;
//	int* pa = &a;//pa指针变量
//	*pa=20;//解引用操作
//	return 0;
//}

//void Swap1(int x, int y)
//{
//	int z = 0;
//	z = x;
//	x = y;
//	y = z;
//}
//void Swap2(int* pa, int* pb)
//{
//	int tmp = 0;
//	tmp=*pa;
//	*pa = *pb;//传址调用
//	*pb=tmp;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	scanf("%d %d", &a, &b);
////调用Swap1函数-传值调用
//	//Swap1(a, b);
////调用Swap2函数-传值调用
//	Swap2(&a, &b);
//	printf("a=%d b=%d\n", a,b);
//	return 0;
//}

////1.写一个函数可以判断一个数是不是素数。
//void sushu(int i, int j)
//{
//	for (j = 2; j < i; j++)
//		if (i%j == 0)
//		{
//		printf("这个数不是素数");
//		}
//		else
//		{
//			printf("这个数是素数");
//		}
//}
//int main()
//{
//	int i = 0;
//	int j = 0;
//	scanf("%d\n", &i);
//	sushu(i,j);
//	return 0;
//}this is by me,that is fault.

//是素数返回1，不是素数返回0
int is_prime(int n)
{
	//2-->n-1
	int j = 0;
	for (j = 2; j < n; j++)
	{
		if (n%j == 0)
			return 0;
	}
	return 1;
}
int main()
{
	//打印100-200之间的素数
	int i = 0;
	for (i = 100; 1 <= 200; i++)

	{
		//判断i是否为素数
		if (is_prime(i) == 1)
			printf("%d", i);
	}
	return 0;
}

//int sushu(int i, int j)
//{
//	for (j = 2; j < i; j++)
//		if (i%j == 0)
//		{
//		return 0;
//		}
//		else
//		{
//			return 1;
//		}
//}
//int main()
//{
//	int i = 0;
//	int j = 0;
//	for (i = 100; i <= 200; i++)
//	{
//		if (sushu(i,j) == 1)
//			printf("%d", i);
//	}
//	return 0;
//}
