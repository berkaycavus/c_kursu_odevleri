
```
#include <stdio.h>

int main()
{
	int x = -1;
	long y = -2;
	long long z = -3;

  //x, y ve z değişkenlerinin değerlerini standart output'a yazdıran tek bir printf çağrısı gerçekleştirin.
}

````
------------------------------------------------------------------------------------------------------------
````
/*	
	author	: bc
	date	: 03.01.2022
*/
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>

int main()
{
	int x = -1;
	long y = -2;
	long long z = -3;

	//x, y ve z değişkenlerinin değerlerini standart output'a yazdıran tek bir printf çağrısı gerçekleştirin.

	printf("\nint x = %d, long y = %ld, long long z = %lld ", x, y, z);
}
````
