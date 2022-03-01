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
- [ls](https://en.wikipedia.org/wiki/Ls)
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
    
  `$ cd ~/boost_1_69_0` - переходим в рабочий каталог /boost_1_69_0
  
  3. Для того, чтобы посдчитать количество файлов в директории ~/boost_1_69_0 ,не включая вложенные директории, т.е. ***всех количество файлов и деректорий в текущем каталоге*** используем комбинацию:

` ls | wc -l` 
- ls - команда, отображающая список файлов и подкатологов, находящихся в конкретном каталоге 
- wc - позволяет подсчитать количество строк, слов, символов и байтов в каждом заданном файле или стандартном вводе и распечатать результат

4. Дла подсчета количества файлов в директории ~/boost_1_69_0 включая вложенные директории, необходимо использовать комбинацию:

`-type f | wc -l` - ***количество файлов в нынешной директории и всех ее поддиректориях***
`find . -type f -name "*.txt" | wc -l` - ***команда рекурсивно считает число файлов с расширением «.txt» в текущей директории и всех ее поддиректориях***
 
   
 
  
  
  
