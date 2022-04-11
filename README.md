#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>


void JUMP(int start, int jump, int end)
{
	int i;
	for (i = start;i <= end;i = i + jump)
	{
		printf("%d,", i);
	}
}


void main()
{
	windows:
	int start, jump, end;
	printf("gimme 3 numbers.\n");

	printf("start with....\n");
	scanf_s("%d", &start);

	printf("jump...\n");
	scanf_s("%d", &jump);

	printf("end with...\n");
	scanf_s("%d", &end);

	if (start >= end)
	{
		printf("theres a problem! please try again.\n");
		goto windows;
	}

	JUMP(start, jump, end);

	system("pause");
}
