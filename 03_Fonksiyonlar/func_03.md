#### Kendisine gün, ay ve yıl olarak gönderilen tarihin yılın kaçıncı günü olduğunu hesaplayan _day_of_year_ isimli işlevi tanımlayın:

```
int day_of_year(int day, int mon, int year);
```

+ İşlevin geri dönüş değeri _day/month/year_ tarihinin year yılının kaçıncı günü olduğu bilgisi.
+ Artık yılları _(leap years)_ göz önüne almayı unutmayınız.

-----------------------------------------------------------------------------------------------------------------------------------------
```
/*	
	author	: bc
	date	: 02.01.2022
	max component
*/
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>

int isleap(int y){
	//printf("%d", (y % 4 == 0 && y % 100 != 0) || y % 400 == 0);
	return (y % 4 == 0 && y % 100 != 0) || y % 400 == 0;
}

int day_of_year(int day, int mon, int year) {

	double sum_month = 0, mult_month = 0;

	for (int i = 1; i < mon; ++i) {
		if (i == 1 || i == 3 || i == 5 || i == 7 ||
			i == 8 || i == 10 || i == 12) {
			sum_month += 31;
		}


		else if (i == 2) {
			if (isleap(year))
				sum_month += 29;
			else
				sum_month += 28;
		}

		else if (i == 4 || i == 6 || i == 9 || i == 11)
			sum_month += 30;
	}
	day = (double)day;
	return sum_month + day;
}

int main()
{
	int iday = 0, imonth = 0, iyear = 0;
	int w = 0;
	while (1) {
		printf("day.month.year formatında bir tarih giriniz...\n");
		w = scanf("%d.%d.%d", &iday, &imonth, &iyear);

		printf("%d.%d.%d\n", iday, imonth, iyear);

		printf("girilen tarih %d yilinin %d. gunudur...\n", iyear, day_of_year(iday, imonth, iyear));
	}
	
	return 0;
}
```
