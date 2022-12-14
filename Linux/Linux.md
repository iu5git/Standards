# Linux

## Образ для виртуальной машины
- [Ссылка](https://drive.google.com/file/d/1mudkSa8viUku64X_fA54s330IRRGMxp6/view?usp=sharing) для использования образа Linux 20.04 с предустановленным ПО
- Пользователь student
- Пароль 1
- База данных student

## установка всех пакетов 
- [пакеты](packages.md) для прохождения курса бакалавриата ИУ5 МГТУ им. Баумана на Linux

## Использование виртуальной машины

С точки зрения пользователя, виртуальные машины выглядят как реально существующие машины. На одной реальной машине может быть установлено несколько виртуальных, на каждой из которых может быть установлено собственное программное обеспечение. 

## Программа виртуализации Oracle VM VirtualBox
Данная программа виртуализации фирмы Oracle предназначена для создания виртуальных машин, установки на этих машинах операционных систем и работы в среде виртуальных ОС.
Гостевая операционная система в VirtualBox может быть установлена либо с использованием дистрибутива, либо импортом готовой конфигурации, сгенерированной ранее операционной системы.
### 1.Создание виртуальной машины и установка гостевой ОС с использованием дистрибутива.
1.	Выбрать пункт меню «Создать»
2.	Задать:
3.	имя новой виртуальной машины тип устанавливаемой гостевой системы;
4.	определить количество выделяемой ей оперативной памяти;
5.	создать виртуальный диск (фиксированного размера или динамически расширяющийся).
6.	После создания виртуальной машины производится обычная установка гостевой операционной с установочного диска или образа ISO дистрибутива.
### 2. Создание виртуальной машины и установка гостевой ОС путем импорта готовой конфигурации
1.	Выбрать пункт меню «Импорт»
2.	Выбрать устанавливаемую конфигурацию в открытых форматах виртуализации OVA или OVF.
3.	Открывается окно «Укажите параметры импорта»
4.	Перечисляются устройства импортируемой конфигурации.
5.	Некоторые параметры можно изменить или отключить
6.	После этого производится создание новой виртуальной машины и импорт выбранной конфигурации.

## Linux Базовые команды 
https://habr.com/ru/post/481398/

У каждой команды есть много опций, здесь все они перечислены не будут. Всегда можно ввести `man <команда>` или `<команда> --help`, чтобы узнать о команде подробнее.

 ```
 $ mkdir --help
 ```
Если какая-то команда выполняется слишком долго, её можно завершить, нажав в консоли Ctrl+C (процессу посылается сигнал SIGINT).
## pwd
Вывести текущую (рабочую) директорию.
 ```
 $ pwd
 /home/user
 ```
## date
Вывести текущую дату и время системы.
 ```
 $date
 Mon Dec 16 13:37:07 UTC 2022
 ```
## w
Данная команда показывает, кто залогинен в системе. Помимо этого также на экран выводится uptime и LA (load average).

## ls
Вывести содержимое директории. Если не передать путь, то выведется содержимое текущей директории.

Есть 2 специальных имени директории: "." и "..". Первое означает текущую директорию, второе — родительскую директорию. Их бывает удобно использовать в различных командах.
## cd
Изменить текущую директорию.

## mkdir
Создать директорию.

## rm
Удалить файл.

Опция -r позволяет рекурсивно удалять директории со всем их содержимым, опция -f позволяет игнорировать ошибки при удалении (например, о несуществующем файле). Эти опции позволяют, грубо говоря, гарантированно удалить всю иерархию файлов и директорий (если на это есть права у пользователя), поэтому, их нужно использовать с осторожностью (классический пример-шутка — "rm -rf /", при определенных обстоятельствах удалит вам если не всю систему, то очень много важных для её работоспособности файлов).
## cp
Копировать файл или директорию.
 ```
 $ ls
 temp test
 $ cp temp tem_clone
 $ ls
 temp temp_clone test
 ```
## mv
Переместить или переименовать файл или директорию.

## cat
Вывести содержимое файла (или файлов).
```
$ cat temp
Content of a file
Lalalala...
```
 


