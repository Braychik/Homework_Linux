**Используя команду cat, создать два файла с данными, а затем объединить их.**

touch firstfile, touch secondfile

С помощью nano вводим текст в файлы

cat firstfile secondfile > thirdfile

**Просмотреть содержимое созданного файла.**

cat thirdfile

**Переименовать файл, дав ему новое имя.**

mv thirdfile renamefile

--------------------------------------------------------------------------------------------------------
**Создать несколько файлов.**

Использую предыдущий файл

**Создать директорию, переместить файл туда.**

mkdir nfolder

mv renamefile /home/braychik/newfolder/nfolder

**Удалить все созданные в этом и предыдущем задании директории и файлы.**

rm -r nfolder

--------------------------------------------------------------------------------------------------------
**Создать файл file1 и наполнить его произвольным содержимым.**

echo"insert text here" > file1

**Скопировать его в file2.**

cp file1 file2

**Создать символическую ссылку file3 на file1.**

ln -s file1 file3

**Создать жёсткую ссылку file4 на file1.**

ln file1 file4

**Посмотреть, какие айноды у файлов.**

У file1 и file4 одинаковые айноды.

**Удалить file1.**

rm file1
**Что стало с остальными созданными файлами?**

file3 не доступен для чтения

**Попробовать вывести их на экран.**

остальные работают так же

-----------------------------------------------------------------------------------------------------------
**Дать созданным файлам другие, произвольные имена.**

mv file4 f4

**Создать новую символическую ссылку.**

ln -s f4 test

**Переместить ссылки в другую директорию.**

mkdir folder

mv test /home/braychik/newfolder/folder

ссылка после перемещения в другую папку не работает