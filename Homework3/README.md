**Создать два произвольных файла.**

• Первому присвоить права на чтение и запись для владельца и группы, только на чтение — для всех.

• Второму присвоить права на чтение и запись только для владельца. Сделать это в численном и символьном виде.

• Назначить новых владельца и группу для директории целиком.

touch firstfile,
touch secondfile

chmod 554 firstfile,
chmod 500 secondfile

chmod ug=rw,o=r firstfile,
chmod u+rw,go-rwx secondfile

sudo chown braucjik:group2 ./

**Управление пользователями:**
* создать пользователя, используя утилиту useradd и adduser;
* удалить пользователя, используя утилиту userdel.

sudo useradd -s /bin/bash -m -d /home/braychik braychik

sudo adduser braychik

sudo userdel braychik

**Управление группами:**

Создать группу с использованием утилит groupadd и addgroup.

попрактиковаться в смене групп у пользователей;

добавить пользователя в группу, не меняя основной;

• Создать пользователя с правами суперпользователя. Сделать так, чтобы sudo не требовал пароль для выполнения команд.

sudo addgroup groupname

sudo groupadd groupname

sudo usermod -aG groupname braychik

sudo usermod -aG GROUP1,GROUP2,...,GROUPN braychik

sudo usermod -g groupname braychik

sudo usermod -aG root braychik

sudo usermod -aG sudo braychik

sudo visudo

%sudo   ALL=(ALL:ALL) NOPASSWD:ALL