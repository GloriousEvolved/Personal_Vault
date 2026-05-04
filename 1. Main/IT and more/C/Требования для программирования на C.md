---
date: 2025-12-17
formal_date: Wednesday 17th December 2025
tags:
  - IT
  - coding
  - C
---

Сначало нужно ещё установить C компилятор, для того, чтобы запускать код на Windows:
> [!faq]- [Как правильно установить C на Windows 10? - Stack Overflow на русском](https://ru.stackoverflow.com/questions/1449733/%D0%9A%D0%B0%D0%BA-%D0%BF%D1%80%D0%B0%D0%B2%D0%B8%D0%BB%D1%8C%D0%BD%D0%BE-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-c-%D0%BD%D0%B0-windows-10)
>1. установите gcc(mingw) (в том же комплекте есть c++ для с++, gcc именно для си)\
>   - mingw gcc в гугле - первая ссылка/downloads [mingw-w64.org/downloads](https://mingw-w64.org/downloads) [ссылка сразу на скачивание из Github](https://github.com/skeeto/w64devkit/releases) (w64devkit он там называется, не пугайтесь что там написано c,c++, fortran там будет несколько РАЗНЫХ компиляторов) Там находите вашу ОС(Windows), качаете, открываете и устанавливаете в удобную, для вас, папку (компиляторы скорее всего после установки будут в папке bin(а папка bin внутри той папки, куда вы установите весь этот пакет))  
>- добавьте в path путь где лежит установленный gcc\ - [Как добавить путь в переменную среды PATH в Windows \| remontka.pro](https://remontka.pro/add-to-path-variable-windows/). Нужно прописать `sysdm.cpl` в командной строке `WIN + R` или в поиске Windows просто напиши "Изменение системных переменных среды", зайди в раздел "Дополнительно" → "Переменные среды" → Дважды нажать на "PATH" в разделе "Переменные среды пользователя" → "Создать" → Прописать путь до компилятора `gcc.exe`, он обычно лежит в папке `bin`. *Пример:* `F:\Games for Murat\C\w64devkit\bin`.
>Для проверки, что всё сделано правильно зайди в терминал (командная строка или VS Code) и введи команду `gcc --version`. При успешной установке и настройке будет такое сообщение:
>```
>gcc.exe (GCC) 15.2.0
>Copyright (C) 2025 Free Software Foundation, Inc.
>This is free software; see the source for copying conditions.  There is NO 
>warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
>```

Ещё нужно установить [C/C++ компилятор](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) и [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) для запуска кода в терминале VS Code.

В настройках C/C++ компилятора поставь галочки на двух пунтках: [Clear Previous Output](vscode://settings/code-runner.clearPreviousOutput) для очистки результатов прошлых запусков программы, и [Save File Before Run](vscode://settings/code-runner.saveFileBeforeRun) для сохранения файла перед запуском.

### >>> [[Начало работы с C]]