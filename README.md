# Калькулятор на C/C++

Калькулятор это проект на С/С++, который выполняет математические действия относительно выражения, которое пользователь передал на вход.
Он поддерживает стандартные математические операторы, скобки, а также набор встроенных математических функций. Также можно настроить поддержку переменных из файла, которые можно использовать в будущем в своих выражениях.

----

# Оглавление
- [Рекомендованные требования](#рекомендованные-требования)
- [Установка](#установка)
- [Описание](#описание)
- [Команды ускоряющие работу с калькулятором](#Команды-ускоряющие-работу-с-калькулятором)
- [Примеры использования](#примеры-использовния)

# Рекомендованные требования
> - ОС: macOS Big Sur
> - Версия CMake: 3.20
> - Версия Clang: 13.0.0

[🔝Оглавление](#оглавление)

# Установка
1. Клонируем репозиторий на компьютер
```
$ git clone https://github.com/Tsygankov-Slava/Calculator.git
 ```
2. Перейдём в папку `./Calculator`с проектом
```
$ cd Calculator
```
3. Создадим папку с именем `build`, куда будем собирать проект и перейдём в неё
```
$ mkdir build
$ cd build
```
4. Теперь следует выполнить команду `cmake`, куда передадим в аргумент файлы проекта, чтобы у нас создались необходимые файлы для самой сборки
```
$ cmake ../
-- The CXX compiler identification is AppleClang 13.0.0.13000029
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /Users/tv/Desktop/Calculator/build
```
5. Выполним команду `make` для сборки проекта
```
$ make
[ 11%] Building CXX object CMakeFiles/Calculator.dir/src/main.cpp.o
[ 22%] Building CXX object CMakeFiles/Calculator.dir/src/File/File.cpp.o
[ 33%] Building CXX object CMakeFiles/Calculator.dir/src/Variables/Variables.cpp.o
[ 44%] Building CXX object CMakeFiles/Calculator.dir/src/Token/Token.cpp.o
[ 55%] Building CXX object CMakeFiles/Calculator.dir/src/RPN/RPN.cpp.o
[ 66%] Building CXX object CMakeFiles/Calculator.dir/src/isDebug/isDebug.cpp.o
[ 77%] Building CXX object CMakeFiles/Calculator.dir/src/Debug/Debug.cpp.o
[ 88%] Building CXX object CMakeFiles/Calculator.dir/src/Containers/Vector/Vector.cpp.o
[100%] Linking CXX executable Calculator
[100%] Built target Calculator
```
6. Наш проект собрался и исполняемый файл лежит в папке `build`, откуда в дальнейшем мы будем запускать наш проект ([см. пункт "Пример использования"](#пример-использовния))

[🔝Оглавление](#оглавление)

#  Описание
### Консольный калькулятор содержит:
> - [Основные операции с числами {"+", "-", "*", "/"}](#основные-операции-с-числами)
> - [Поддержка скобок в выражениях](#поддержка-скобок-в-выражениях)
> - [Основные функции {"sqrt", "log",  "sin", "cos", "exp", "real", "imag", "phase", "mag"}](#основные-функции)
> - [Константы](#константы)
> - [Переменные](#переменные)

[🔝Оглавление](#оглавление)

# Основные операции с числами
- ### Операция сложения
  ```
  Введите выражение -> 2 + 4

  Ответ: 6.000000 + 0.000000i
  ```
- ### Операция вычитания
  ```
  Введите выражение -> 2 - 5

  Ответ: (-3.000000) + 0.000000i  
  ```
- ### Операция умножения
  ```
  Введите выражение -> 4 * 9

  Ответ: 36.000000 + 0.000000i  
  ```
- ### Операция деления
  ```
  Введите выражение -> 9 / 4

  Ответ: 2.250000 + 0.000000i
  ```

[🔝Оглавление](#оглавление)

# Поддержка скобок в выражениях
  ```
  Введите выражение -> (2 + 2) * 2

  Ответ: 8.000000 + 0.000000i
  ```

[🔝Оглавление](#оглавление)

# Основные функции
- ### Функция квадратного корня
  ```
  Введите выражение -> sqrt(9 + 7) 

  Ответ: 4.000000 + 0.000000i
  ```
- ### Функция логарифма
  ```
  Введите выражение -> log(E + PI)

  Ответ: 1.768128 + 0.000000i
  ```
- ### Функция синуса
  ```
  Введите выражение -> sin(-E)

  Ответ: (-0.410781) + 0.000000i
  ```
- ### Функция косинуса
  ```
  Введите выражение -> cos(PI)

  Ответ: (-1.000000) + 0.000000i
  ```
- ### Функция экспоненты
  ```
  Введите выражение -> exp(E)

  Ответ: 15.154265 + 0.000000i
  ```
- ### Функция взятия действительной части комплексного числа
  ```
  Введите выражение -> real(2.4 + 2.3i)

  Ответ: 2.400000 + 0.000000i
  ```
- ### Функция взятия мнимой части комплексного числа
  ```
  Введите выражение -> imag(2.4 + 2.3i)

  Ответ: 2.300000 + 0.000000i
  ```
- ### Функция `phase`
  ```
  Введите выражение -> phase(1 + i)

  Ответ: 0.785398 + 0.000000i
  ```
- ### Функция `mag`
  ```
  Введите выражение -> mag(1 + i)

   Ответ: 1.414214 + 0.000000i
  ```

[🔝Оглавление](#оглавление)

# Константы
- `PI = 3.14159` (Число pi)
- `E = 2.71828` (Число Эйлера)

[🔝Оглавление](#оглавление)

# Переменные

❗Переменные можно задавать двумя способами

## `Способ №1`
Чтобы использовать переменные, надо создать файл с расширением `.txt` (в любом месте), затем указать путь к этому файлу при запуске программы с флагом `-variables` (см. пример ниже).

❗Объявлять переменные можно в любом порядке

Пример файла `variables.txt` с некоторым количеством переменных
```
x = 1.3 + PI*i
y = exp(x)
z = x + y
ddx = z^2 + 1
xyz = x + y + z + ddx
```
В данном примере объявлено 5 переменных `{x, y, z, ddx, xyz}`

Пример запуска программы с указанием того, что в математических выражениях будут использоваться переменные из файла `/Users/tv/Desktop/variables.txt`
```
$ ./Calculator -variables /Users/tv/Desktop/variables.txt
```

## `Способ №1`

Переменные можно вводить прям при подсчёте выражения, для этого стоит просто написать `имя_переменной = значение`, затем они сами добавятся в файл с переменными

```
Введите выражение или команду -> -out all
Не обнаружено переменных в файле!
Введите выражение или команду -> a = 5
Переменная успешно добавлена!

Введите выражение или команду -> b = 2
Переменная успешно добавлена!

Введите выражение или команду -> -out all
Переменные из файла: 
Кол-во переменных -> 2
|---------
|a = 5
|b = 2
|---------
```

[🔝Оглавление](#оглавление)

# Команды ускоряющие работу с калькулятором

- `-help` -> Подскажет всевозможные команды
- `-out all` -> Выведет файл с переменными
- `-out var` -> Выведет значение переменной var, можно через запятую [var1,var2] 
- `-del all` -> Удалит весь файл с переменными
- `-del var` -> Удалит переменную из файла
- `-exit` -> Завершит работу калькулятора                                        

Примеры использования:
```
Введите выражение или команду -> -help
|------------------------------------------------------------------------------|
| -help -> Подскажет всевозможные команды                                      |
| -out all -> Выведет файл с переменными                                       |
| -out var -> Выведет значение переменной var, можно через запятую [var1,var2] |
| -del all -> Удалит весь файл с переменными                                   |
| -del var -> Удалит переменную из файла                                       |
| -exit -> Завершит работу калькулятора                                        |
|------------------------------------------------------------------------------|
```

```
Введите выражение или команду -> -out all
Переменные из файла: 
Кол-во переменных -> 5
|---------
|ddx = ((1.3+PI*i)+(exp((1.3+PI*i))))^2+1
|x = 1.3+PI*i
|xyz = (1.3+PI*i)+(exp((1.3+PI*i)))+((1.3+PI*i)+(exp((1.3+PI*i))))+(((1.3+PI*i)+(exp((1.3+PI*i))))^2+1)
|y = exp((1.3+PI*i))
|z = (1.3+PI*i)+(exp((1.3+PI*i)))
|---------
```

```
Введите выражение или команду -> -out ddx,x,z
|ddx = ((1.3+PI*i)+(exp((1.3+PI*i))))^2+1
|x = 1.3+PI*i
|z = (1.3+PI*i)+(exp((1.3+PI*i)))
```

```
Введите выражение или команду -> -del ddx,x
Переменная ddx успешно удалена из файла!
Переменная x успешно удалена из файла!
Введите выражение или команду -> -out all
Переменные из файла: 
Кол-во переменных -> 3
|---------
|xyz = x+(exp(x))+(x+(exp(x)))+ddx
|y = exp(x)
|z = x+(exp(x))
|---------
```

```
Введите выражение или команду -> -del all
Файл успешно очищен!
Введите выражение или команду -> -out all
Не обнаружено переменных в файле!
```

```
Введите выражение или команду -> -exit
Калькулятор закончил работу!
```

[🔝Оглавление](#оглавление)

# Примеры использовния
После успешной установки и сборки проекта запустим его.

❗Существует два способа посчитать математическое выражение

## `Способ №1`

1. Для этого откроем терминал(консоль) и перейдём в папку с исполняемым файлом.
```
$ cd Calculator/build
```

2. Запустим наш исполняемый файл, передав в качестве аргументов путь к файлу с переменными (через флаг `-variables`).
```
$ ./Calculator -variables /Users/tv/Desktop/variables.txt
```

3. Наш калькулятор запустился, если всё прошло успешно он попросит ввести выражение.

4. Попробуем ввести выражение `sin(x + y) * (xyz + ddx + z + y)`

Наши переменные в файле (их можно ввести двумя способами [см. пункт "Переменные"](#переменные)):
```
x = 1.3 + PI*i
y = exp(x)
z = x + y
ddx = z^2 + 1
xyz = x + y + z + ddx
```

Выражение и ответ:
```
Введите выражение -> sin(x + y) * (xyz + ddx + z + y)

Ответ: (-28.487308) + 307.618134i
```

## `Способ №2`

1. Для этого также откроем терминал(консоль) и перейдём в папку с исполняемым файлом.
```
$ cd Calculator/build
```

2. Запустим наш исполняемый файл, передав в качестве аргументов путь к файлу с переменными (через флаг `-variables`) и
   математическое выражение (через флаг `-exp`).

❗Математическое выражение при вводе его через флаг `-exp` при запуске должно находится всегда на последнем месте.

```
$ ./Calculator -variables /Users/tv/Desktop/variables.txt -exp sin(x + y) * (xyz + ddx + z + y)
```

Вывод:
```
Полученное выражение -> sin(x+y)*(xyz+ddx+z+y)

Ответ: (-28.487308) + 307.618134i
```

[🔝Оглавление](#оглавление)