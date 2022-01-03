Aşağıdaki program derlenip çalıştırıldığında ekran çıktısı ne olur?
  
```
#include <stdio.h>

int main()
{
	int x = 333;

	printf("%d", printf("%d", printf("%d", x)));
}

```
-------------------------------------------------------------------
```
--> 33331

ilk printf 333, daha sonraki ilkinin geri dönüş değerini yani 3, en son ki 2. nin ger, dönüş değerini yani 1
```
