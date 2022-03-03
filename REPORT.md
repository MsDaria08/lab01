
### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix)) cоздание и управление архивами библиотек
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix)) объединение и вывод файлов 
- [cd](https://en.wikipedia.org/wiki/Cd_(command)) смена рабочей директории 
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix)) копирование файлов
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix)) вырезание части текста
- [echo](https://en.wikipedia.org/wiki/Echo_(command)) выводит строку текста в терминал
- [env](https://en.wikipedia.org/wiki/Env_(shell)) используется либо для печати списка переменных среды
- [ex](https://en.wikipedia.org/wiki/Ex_(editor)) текстовый редактор (режим строчного редактора)
- [file](https://en.wikipedia.org/wiki/File_(command)) позволяет узнать тип данных, которые содержатся внутри документа
- [find](https://en.wikipedia.org/wiki/Find) команда для поиска файлов и каталогов
- [ls](https://en.wikipedia.org/wiki/Ls) выводит список файлов в директории 
- [man](https://en.wikipedia.org/wiki/Man_page) позволяет получить доступ к общей базе справки по команде, функции или программе
- [mkdir](https://en.wikipedia.org/wiki/Mkdir) cоздание новых директорий.
- [mv](https://en.wikipedia.org/wiki/Mv) переместить (или переименовать) файлы или директории
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix)) печатает информацию о бинарных файлах
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd) позволяет вывести в терминал путь к текущей папке
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix)) удаление файлов и директорий
- [sed](https://en.wikipedia.org/wiki/Sed)потоковый редактор текста, работающий по принципу замены, его можно использовать для поиска, вставки, замены и удаления фрагментов в файле
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix)) //создание пустого файла

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software))(Advanced Packaging Tool) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details) - набор библиотек, в которых реализуются базовые возможности работы с URL страницами и передачи файлов. `$ curl опции ссылка`
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf) загрузка файлов, скриптов, загрузочных пакетов... Работает по протоколам HTTP, HTTPS и FTP. `$ wget опции аддресс_ссылки`
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html) команда, предназначена для компиляции с помощью компилятора GCC кода на языке C++ `$ g++ [параметры] имена файлов`
- [make](https://en.wikipedia.org/wiki/Make_(software)) - утилита предназначенная для автоматизации преобразования файлов из одной формы в другую.
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html) -позволяет открыть файл
- [openssl](https://www.openssl.org) - набор инструментов для криптографии
- [nano](https://www.nano-editor.org) - текстовый редактор
- [tree](https://linux.die.net/man/1/tree) - это рекурсивная программа для составления списка каталогов. Без аргументов в дереве перечислены файлы в текущем каталоге. Когда задаются аргументы каталога, в дереве по очереди перечисляются все файлы и/или каталоги, найденные в заданных каталогах. По завершении перечисления всех найденных файлов/каталогов tree возвращает общее количество перечисленных файлов и/или каталогов.
- [vim](http://www.vim.org) - свободный текстовый редактор


 ## Homework
1. Скачиваем библиотеку boost с помощью утилиты wget:
 
  ` $ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz` 
  
  
2. Разорхивируем скаченную библиотеку в директорию ~/boost_1_69_0 :
    
  `$ tar -xf boost_1_69_0.tar.gz`
  ```cpp
  -extract ( -x ) — Извлечь весь архив или один или несколько файлов из архива (operation)
  -file=archive=name ( -f archive-name ) — указывает имя файла архива (option)
  ```
   
  ![изображение_1] ( https://raw.githubusercontent.com/MsDaria08/lab01/master/1.jpg )
   
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
 
 + `find -type f ! -name "*.cpp" -a ! -name "*.hpp" -a ! -name "*.h" | wc -l` 
                  где - а - опрервтор логического И
 
 6. Находясь в директории /boost_1_69_0, используем команду:
 
 `find $PWD -type f -name "any.hpp"`
      pwd - команда вывода в терминал путь к текущей папке
 
 
 7. Находясь в директории /boost_1_69_0, используем команду:
 
 `grep -rl boost::asio`
 ```cpp
  -r (--recursive) - осуществляет поиск по всем файлам в указанном каталоге
  -l - вывод по умолчанию и печатать только имена файлов
  ```
  
 8. Скомпилируем boost. Можно воспользоваться инструкцией или ссылкой.
 
 `$ ./bootstrap.sh`
 `$ ./b2`


9. Все скомпилированные на предыдущем шаге статические библиотеки сохранились в директорию `stage/lib`, перенесем все данные в диреткорию `~/boost-libs` с помощью команды: 


 
                      
  
  
  
