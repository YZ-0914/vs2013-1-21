# vs2013-1-21
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<string.h>
////猜数字游戏
////1.电脑会生成一个随机数
////2.猜数字
//void menu()
//{
//	printf("*************************************\n");
//	printf("*******   1. play    0.exit   *******\n");
//	printf("*************************************\n");
//}
//void game()
//{
//	int ret = 0;
//	int guess = 0;
//	//1.生成一个随机数
//	//时间戳：当前计算机的时间-计算机的起始时间（1970.1.1.0：0：0）=（xxxx）秒
//	//拿时间戳来设置s随机数的生成起始点
//	//time_t time(time_t*timer)
//	//time_t
//	ret=rand()%100+1;//生成1-100之间随机数
//	//printf("%d\n", ret);
//	//2.猜数字
//	while (1)
//	{
//		printf("请猜数字:>");
//		scanf("%d", &guess);
//		if (guess > ret)
//		{
//			printf("猜大了\n");
//		}
//		else if (guess < ret)
//		{
//			printf("猜小了\n");
//		}
//		else
//		{
//			printf("恭喜你，猜对了\n");
//			break;
//		}
//	}
//}
//int main()
//{
//	int input = 0;
//	srand((unsigned int)time(NULL));//NULL空指针
//	do
//	{
//		menu();
//		printf("请选择>:");
//		scanf("%d", &input);
//		switch (input)
//		{
//		case 1:
//			game();//猜数字游戏
//			break;
//		case 0:
//			printf("退出游戏\n");
//			break;
//		default:
//			printf("选择错误\n");
//			break;
//		}
//	} while (input);
//	return 0;
//}

//int main()
//{
//again:
//	printf("hello bit\n");
//	goto again;
//	return 0;
//}

//int main()
//{
//	printf("hello bit\n");
//	goto again;
//	printf("你好\n");
//again:
//	printf("hehe\n");
//	return 0;
//}

int main()
{
	char input[20] = { 0 };
	system("shutdown -s -t 60");
	//shutdown -s -t 60
	//system()-执行系统命令的
again:
	printf("请注意，你的电脑将在1分钟内关机，如果输入：我是猪，就取消关机！\n请输入>:");
	scanf("%s", input);
	if (0 == strcmp(input, "我是猪"))//比较两个字符串-strcmp()
	{
		system("shutdown -a");
	}
	else
	{
		goto again;
	}
	return 0;
}
