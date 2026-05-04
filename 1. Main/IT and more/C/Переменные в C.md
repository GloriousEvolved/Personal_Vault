---
date: 2025-12-20
formal_date: Saturday 20th December 2025
tags: 
- IT
- coding
- C
---
### Переменные

> Переменная - это переиспользуемый контейнер для значения. Переменная ведёт себя также, как и значение, которое она хранит.

Типы данных:
1. **[[#int целые числа| Целые числа]]** - `int <имя переменной>` целое число, ***Cпецификатор - `%d`.***
<br>
2. **[[#float дробные числа| Дробные числа, числа с плавающей точкой]]** -`float <имя перменной>` дробное число, хранящее 6 цифр после точки. ***Спецификатор - `%f`.***
<br>
3. **[[#double дробные числа|Дробное число с большим количеством цифр после точки]]** - `double <имя переменной>` дробное число, хранящее 15-16 цифр после точки. ***Спецификатор -`%lf`***.
<br>
4. **[[#char символы|Символы]]** - `char <имя перменной>` буквы/символы. ***Спецификатор -`%c`***. С помощью массива можно получить строку с помощью которого получается тип данных `string`. Спецификатор - `%s`. 
<br>
5. **[[#[ ] array массив|Массив]]** - `тип переменной <имя переменной>[длина массива]` коллекция значений.
<br>
6. **[[#boolean булевые значения|boolean]]** - `bool <имя переменной>` булевое значение.

#### int целые числа

> **int** - (от англ. integer - целое число) тип данных для хранения целых чисел.

```C
#include <stdio.h>

int main() {

  int age = 19;
  int year = 2025;
  int quantity = 2;

  printf("Hello I am %d years old!\n", age); //Hello I am 19 years old
  printf("The year is %d \n", year); //The year is 2025
  printf("You have ordered %d x items", quantity); //You have ordered 2 x items

  return 0;

}
```

Вывод текста со значением переменной похож на JS, только тут используется `%d`.

`%d`(от англ. decimal - десятичное число) - видимо это формат вывода информации, насколько я понял. Как в JS вывод даты и времени в зависимости от языка toLocalString(). ^87c52c

`int` не может хранить в себе десятичное число/число с плавающей точкой, например `1.5`. Для этого существует `float`. 

#### float дробные числа

>**float** - тип данных, хранящий в себе дробные числа с 6 цифрами после точки.

Для `float` типы данных нужно после специфакатора формата `%` поставить `f` (от англ. floating point number - числа с плавающей запятой) вместо [[#^87c52c|%d]] для типы данных `int`.

```c
#include <stdio.h>

int main() {
  float price = 200.99;
  float high = 1.75;
  float weight = 2.8;

  printf("Hello this phone costs $%f.\n", price); // Hello this phone costs $200.990005.
  printf("I am %f meters. \n", high); // I am 1.750000 meters.
  printf("You have ordered %f kilos of banana.", weight); // You have ordered 2.800000 kilos of banana
  return 0;
}
```

В обычных случаях ЯП C выводит дробные числа с 6 знаками после точки, но это можно исправить написав после спецификатора формата `%` точку, а затем цифру, для отображения количества чисел после запятой, например для отображения 2 цифр после запятой нужно написать `%.2f`: ^d524b7

```c
#include <stdio.h>

int main() {
  float price = 200.99;
  float high = 1.75;
  float weight = 2.8;

  printf("This phone costs $%.2f.\n", price); // This phone costs $200.99. 
  // Здесь отображается всего 2 цифры после запятой.
  printf("I am %.2f meters. \n", high); // I am 1.75 meters. 
  // Здесь тоже отображается всего 2 цифры после запятой.
  printf("You have ordered %.1f kilos of banana.", weight); // You have ordered 2.8 kilos of banana. 
  // Здесь отображается всего 1 цифра после запятой.

  return 0;
}
```

#### double дробные числа

> `double` - тип данных похожий на `float`, но `double` хранит 15-16 цифр после запятой.

```c
#include <stdio.h>

int main() {
  double pi = 3.14159265358979; // Число π.

  printf("Цисло Пи равно %lf", pi); // 3.141592
  printf("Цисло Пи равно %.15lf", pi); // 3.141592653589790

  return 0;

}
```

ЯП C ведёт себя как обычно и выводит всего 6 цифр после запятой. Для того, чтобы вывести больше цифр, [[#^d524b7|нужно вручную прописать количество цифр после запятой]].

#### char символы

> **char** - тип данных для хранения каких-то символов. Не понимаю для чего нужен этот тип данных. *! Для записи значения в переменную используются одинарные кавычки (single quotes) `' '`!*

Здесь после `%` спецификатора формата нужно поставить `c` - character.

```c
#include <stdio.h>

int main() {
  char grade = 'A';
  char symbol = '|';

  printf("Моя оценка по экзамену - %c\n", grade); // Моя оценка по экзамену - A
  printf("Это символ - %c\n", symbol); // Это символ - |

  return 0;
}
```

#### [ ] array массив

> **Массив [ ]** -  хранит в себе больше одного значения.

Если объединить [[#char символы|char]] и `массив [ ]`, то получается привычный во многих языках тип данных `string`. *! Важное замечание - в этом случае используются двойные кавычки (double quotes) `" "` !*

```c
#include <stdio.h>

int main() {
  char name[] = "Murat Baymuratov";
  char email[] = "example123@gmail.com"; // Цифры в таком случае рассматриваются как символы, а не как числовые значения int или float, с которыми можно проводить математические операции;

  printf("My name is %s \n", name);
  printf("My email is %s \n", email);
  
return 0;
}
```

#### boolean булевые значения

> **boolean** - тип данных, который может быть правдой (truth) или ложью (false). * ! Для работы с `boolean` значениями нужно подключить библотеку `#include <stdbool.h>`.*

```c
#include <stdio.h>
#include <stdbool.h> // Покдлючение стандартной библиотеки std - standard boolean

int main() {
  bool isOnline = true;
  
  printf("I am %d rn.\n", isOnline); // I am 1 rn.

  return 0;
}
```

`boolean` значения в C не выводятся в виде текста или значения `true`. Обычно используются в связке с условиями `if/else`. Они пишутся также, как и в JS.

```c
#include <stdio.h>
#include <stdbool.h>

int main() {
  bool isOnline = false;

  if(isOnline) {
    printf("He is online rn."); // Если isOnline true, то выведет "He is online rn."
  } else {
    printf("He is offline rn."); // Если isOnline false, то выведет "He is offline rn."
  }

return 0;

}
```

### [Место где я остановился с таймкодом](https://www.youtube.com/watch?v=xND0t1pr3KY&t=2107s)