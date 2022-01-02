* _4_ sayıdan en büyüğünü hesaplayan _max4_ isimli bir fonksiyon tanımlayınız.

* _main_ fonksiyonu içinde standart giriş akımından _4_ tamsayı alınız.

* _max4_ isimli fonksiyona çağrı yaparak alınan _4_ tam sayıdan en büyüğünü standart çıkış akımına _(ekrana)_ yazdırınız:

### Örnek ekran çıktısı (1)

```
dört tamsayi girin:
12 56 91 8

12, 56, 91 ve 8 sayilarinin en buyugu 96
```
-------------------------------------------------------------------------------------------------------------------------

```
/*	
	author	: bc
	date	: 02.01.2022
	max component
*/
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
double array[5] = { 0 };

void max3(int a, int b, int c) {

	if (a > b)
		if (a > c)
			printf("en buyuk sayi = %d", a);
	if (b > a)
		if (b > c)
			printf("en buyuk sayi = %d", b);
	if (c > a)
		if (c > b)
			printf("en buyuk sayi = %d", c);
}

void _max3(int a, int b, int c) {

	if (a > b)
		if (a > c)
			printf("en buyuk sayi = %d", a);
	else if (b > a)
		if (b > c)
			printf("en buyuk sayi = %d", b);
	else 
		printf("en buyuk sayi = %d", c);
}

void _max3_(void) {
	double backup = 0;
	for (int i = 0; i <= 3; ++i) {

		if (array[i] >= array[i + 1])
			array[i + 1] = array[i], backup = array[i + 1];
		
	}
	printf("\n en buyuk sayi = %lf \n", backup);
}

int main()
{
	float x = 0, y = 0, z = 0, t = 0;
	int w;
	printf("Bir sayi giriniz...");
		w = scanf("%f", &x);
		array[0] = x;
	printf("Bir sayi giriniz...");
		w = scanf("%f", &y);
		array[1] = y;
	printf("Bir sayi giriniz...");
		w = scanf("%f", &z);
		array[2] = z;

	printf("Bir sayi giriniz...");
		w = scanf("%f", &t);
		array[3] = t;
	printf("%lf - %lf - %lf", array[0], array[1], array[2]);
	_max3_(x, y, z);
	return 0;
}
```
