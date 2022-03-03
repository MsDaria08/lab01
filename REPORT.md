### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix)) cоздание и управление архивами библиотек
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix)) объеинение и вывод файлов 
- [cd](https://en.wikipedia.org/wiki/Cd_(command)) смена рабочей директории 
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix)) копирование файлов
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix)) 
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls) выводит список файлов в директории 
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)


 ## Homework
1. Скачиваем библиотеку boost с помощью утилиты wget:
 
  ` $ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz` 
  
  
2. Разорхивируем скаченную библиотеку в директорию ~/boost_1_69_0 :
    
  `$ tar -xf boost_1_69_0.tar.gz`
  ```cpp
  -extract ( -x ) — Извлечь весь архив или один или несколько файлов из архива (operation)
  -file=archive=name ( -f archive-name ) — указывает имя файла архива (option)
  ```
    
  `$ cd ~/boost_1_69_0` - переходим в рабочий каталог /boost_1_69_0
  
  
3.  Для подсчета количества  файлов в директории ~/boost_1_69_0 ,***не включая*** вложенные директории, используем:

`ls | wc -l`  - все файлы и директории в текущем каталоге /boost_1_69_0

```cpp
PIPE (|) - это своего рода оператор, который позволяет дополнять выполение разных команд.
```

Если нужно определить количество ТОЛЬКО файлов в текущем каталоге, то используем:

`find . -maxdepth 1 -type f | wc -l`- все файлы в текущем каталоге
  ```cpp
  -maxdepth - глубина обхода католога
  -maxdepth 1- обрабатка всех файлов, кроме начальных точек.
  ````

4. Для подсчета количества файлов в директории ~/boost_1_69_0 , ****включая**** вложенные директории, используем:

  `-type f | wc -l` - все файлы 
  
 ```cpp
  wc (word count — «количество слов») - утилита,выводящая число строк, слов и байт для каждого указанного файла
  
-c 	--bytes 	Отобразить размер объекта в байтах
-m 	--count 	Показать количесто символов в объекте
-l 	--lines 	Вывести количество строк в объекте
-w 	--words 	Отобразить количество слов в объекте
 ```
  
5. Подсчитаем количество заголовочных файлов, файлов с расширением .cpp, сколько остальных файлов (не заголовочных и не .cpp)
 
 + `expr $(find . -type f -name "*.h" | wc -l) + $(find . -type f -name "*.hpp" | wc -l)`  - количество заголовочных файлов
              $() - подстановка системных переменных
    
   или 
   
   `find -name "*.h" -o -name "*.hpp" | wc -l` 
                  где -o - оператор логичесокго ИЛИ (or)
              
 + `find . -type f -name "*.cpp" | wc -l` - количество файлов с расширением .cpp
 
 + find -type f ! -name "*.cpp" -a ! -name "*.hpp" -a ! -name "*.h" | wc -l`\
                  где - а - опрервтор логического И
 
 6. Находясь в директории /boost_1_69_0, используем команду:
 
 `find ~/ -iname "*any.hpp"`
 
 
 7. Находясь в директории /boost_1_69_0, используем команду:
 
 `grep -Rl boost::asio`
 
 
 
 
                      
  
  
  
