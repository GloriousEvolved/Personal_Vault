---
date: 2025-12-17
formal_date: Wednesday 17th December 2025
tags:
  - IT
  - coding
  - C
---
![C Programming Full Course for free ⚙️ (2025) - YouTube](https://youtu.be/xND0t1pr3KY?si=0gk1AgTuuMkKi9nK)

Ссылки:
1. [Язык программирования С (Си) с нуля - CodeBasics](https://code-basics.com/ru/languages/clang)
2. [Курс C- Stepik](https://stepik.org/lesson/1340735/step/1?unit=1356402)
3. [Курс «Введение в C (Си)» hexlet.io](https://ru.hexlet.io/courses/introduction-to-c)

---

> [!warning] 
>  ЯП C не исправляет код за тебя и не ставит `;` (semicolon) сам. Придётся делать всё аккуратно и проставлять `;` в конце строк самому.

Создаём файл `main.c` и прописываем `#include <stdio.h>` - это директива препроцессора для компилятора. Мы подключаем библиотеку ввода-вывода, чтобы выводить результаты кода в терминале.

Для создания функции нужно написать её название `main`, затем круглые скобки и кривые скобки:
```c
#include <stdio.h>

int main() {
	code
}
```

В языке `C` принято начинать программу с главной функции `main` - это точка входа в программу(entry point in your program), место начала запуска программы. 

Есть разные виды функций - одна из них `int`, от слова *integer* целое число. В такой функции в конце обязательно должна быть строчка с возвращением целого числа(integer), в данном случае нуля:

```c
#include <stdio.h> // Покдлючение стандартной библиотеки std - standard, io - input output

int main() {
	
	return 0;
}
```

Возвращение нуля означает, что программа завершена/выполнена успешно. Любое значение отличающееся от нуля обычно указывает на ошибку или проблему. В ранних версиях ЯП C, если не вернуть ноль, то это приводило к неопределённому поведению функции. В новых же версиях эту запись можно опустить (от англ. *omit*), но написание этой строчки является хорошей практикой и она полезна для обратной совместимости.

Для вывода текста в консоль используется команда `printf()`. Текст в `printf()` будет выводиться в одну линию. Для переноса текста на новую строку нужно в месте, где ты хочешь перенести текст написать `\n`. *Здесь "слеш" не обычный `/` (forward slash), а обратный `\` (backward slash).*

```c
#include <stdio.h>

int main() {
  printf("Hello World!\n");
  printf("This is my first programm on C.");  

  return 0;
}
/*Output:
Hello World!
This is my first programm on C.
*/
```

Комментарии на ЯП C такие же как и в JavaScript: однострочный комментарий - два "слеша" (*forward slash*), и многострочный комментарий - *forward slash* 2 звёздочки (*asterisk*) и снова *forward slash*.

```C
#include <stdio.h>

int main() {
  // This is exmaple of a single-line comment

  /*This is
  exmaple
  of a multi-line
  comment
  */

  printf("Hello World!\n");
  printf("This is my first programm on C.");

  return 0;
}
```

### >>> [[Переменные в C]]