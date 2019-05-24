<p align="center">МИНОБРНАУКИ РОССИИ</p>
<p align="center">Федеральное государственное бюджетное образовательное учреждение высшего образования</p>

---

**<p align="center">"МИРЭА – Российский технологический университет"</p>**

**<p align="center">(РТУ МИРЭА)</p>**
**<p align="center">Институт комплексной безопасности и специального приборостроения</p>**

**<p align="center">Кафедра КБ-4 "Автоматизированные системы управления"</p>**

---

**<p align="center">ОТЧЕТ</p>**

<p align="center">по дисциплине "Операционные системы"</p>
<p align="center">по лабораторной работе №2 "RAID"</p>

*<p align="right">Студент:* Симонова Анастасия</p>
*<p align="right">Группа:* ББСО-01-17</p>

<p align="center">Москва</p>
<p align="center">2019</p>

# Задание 1

1. Установка
![1](https://user-images.githubusercontent.com/50047846/58338900-42d1b080-7e51-11e9-99cd-7b423b9e106e.png)
![2](https://user-images.githubusercontent.com/50047846/58342272-e2467180-7e58-11e9-88fd-54c30c77d82e.png)
![3](https://user-images.githubusercontent.com/50047846/58342277-e3779e80-7e58-11e9-8c70-8030098afcf6.png)
---
2. Настройка RAID
![4](https://user-images.githubusercontent.com/50047846/58342278-e3779e80-7e58-11e9-976b-83a7db80df4d.png)
---
3. Настройка LVM
![5](https://user-images.githubusercontent.com/50047846/58342279-e4103500-7e58-11e9-9f80-d409ee3c0b6f.png)
![6](https://user-images.githubusercontent.com/50047846/58342280-e4103500-7e58-11e9-905a-145ee68c26a6.png)
![7](https://user-images.githubusercontent.com/50047846/58342281-e4103500-7e58-11e9-8719-baaaff003657.png)
![8](https://user-images.githubusercontent.com/50047846/58342282-e4103500-7e58-11e9-9abc-eacc5d42786b.png)
---
4. Клонирование содержимого раздела boot с ssd1 на ssd2
![9](https://user-images.githubusercontent.com/50047846/58342284-e4a8cb80-7e58-11e9-9dde-10c1b9c67035.png)
---
5. Вывод fdisk -l
![10](https://user-images.githubusercontent.com/50047846/58342285-e4a8cb80-7e58-11e9-8a04-a25e6b4f0e22.png)
![11](https://user-images.githubusercontent.com/50047846/58342286-e4a8cb80-7e58-11e9-8067-2396cb6c3d33.png)
---
6. Вывод lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINT
![12](https://user-images.githubusercontent.com/50047846/58342287-e5416200-7e58-11e9-91da-edb7bc24408e.png)
---
7. Установка grub на ssd2 и информация о текущем RAID. 
cat /proc/mdstat показывает, что в raid участвуют оба диска.
![13](https://user-images.githubusercontent.com/50047846/58342288-e5416200-7e58-11e9-9594-3f876941223c.png)
---
8. Вывод команд pvs, lvs, vgs
![14](https://user-images.githubusercontent.com/50047846/58342290-e5416200-7e58-11e9-9b5a-085e942dba93.png)
![15](https://user-images.githubusercontent.com/50047846/58342291-e5d9f880-7e58-11e9-9886-fd2d149c75b1.png)
![16](https://user-images.githubusercontent.com/50047846/58342292-e5d9f880-7e58-11e9-8839-bee0f2cde996.png)
---
---
# Задание 2
1. Удаление диска
![17](https://user-images.githubusercontent.com/50047846/58342293-e5d9f880-7e58-11e9-9aa6-52cdb4c9606a.png)
![18](https://user-images.githubusercontent.com/50047846/58342294-e6728f00-7e58-11e9-9344-eee4d7fe222b.png)
---
2. Добавление нового диска
![19](https://user-images.githubusercontent.com/50047846/58342295-e6728f00-7e58-11e9-9be4-01b76aa131f9.png)
---
3. Просмотр результата
![20](https://user-images.githubusercontent.com/50047846/58342297-e6728f00-7e58-11e9-958f-e6843032474e.png)
![21](https://user-images.githubusercontent.com/50047846/58342298-e70b2580-7e58-11e9-865c-a23107a99acc.png)
![22](https://user-images.githubusercontent.com/50047846/58342299-e70b2580-7e58-11e9-9620-e60e1faee4f7.png)
---
4. Копирование таблицы разделов на новый диск
![23](https://user-images.githubusercontent.com/50047846/58342300-e70b2580-7e58-11e9-9257-746dec1c6c52.png)
![24](https://user-images.githubusercontent.com/50047846/58342301-e7a3bc00-7e58-11e9-9df6-aa407d4c557f.png)
![25](https://user-images.githubusercontent.com/50047846/58342303-e7a3bc00-7e58-11e9-80f7-60230d0cafd8.png)
---
5. Добавление RAID-массив нового диска
![26](https://user-images.githubusercontent.com/50047846/58342304-e7a3bc00-7e58-11e9-8a58-bdefa78d6845.png)
![27](https://user-images.githubusercontent.com/50047846/58342305-e7a3bc00-7e58-11e9-80ac-7333d3050d77.png)
---
6. Синхронизация разделов, не входящих в RAID
![28](https://user-images.githubusercontent.com/50047846/58342306-e83c5280-7e58-11e9-9739-c5b6d041b48e.png)
---
7. Установка grub и просмотр RAID-массива
![29](https://user-images.githubusercontent.com/50047846/58342307-e83c5280-7e58-11e9-89bc-64b24ad975fc.png)
---
---
# Задание 3
1. Эмуляция отказа диска ssd2 и просмотр состояния дисков и RAID
![30]()
![31]()
![32]()
![33]()
---
2. Добавление нового диска ssd4, просмотр изменений
![34]()
![35]()
![36]()
---
3.  Копирование файловой таблицы со старого диска на новый
![37]()
![38]()
![39]()\
После выполнения команды sfdisk на новом диске (sdb) появились разделы sdb1 и sdb2.
![40]()
---
4. Скопировали данные /boot с sda1 на sdb1
---
5. Перемонтировали /boot на новый диск (sdb) и установили grub
![41]()
![42]()\
Мы выполнили команду grub-install /dev/sdb, чтобы установить загрузчик группы на новый диск.
---
6. Создаем новый RAID-массив с включением только одного диска sdb
![43]()\
Команда mdadm работает с ключом --force \
Добавился RAID-массив md63 с одним диском \
![44]()\
Отображается в дереве lsblk новый RAID-массив на диске sdb \
Мы выполнили команду grub-install /dev/sdb, чтобы установить загрузчик группы на новый диск.\
---
6. Создаем новый RAID-массив с включением только одного диска sdb
![45]()\
Команда mdadm работает с ключом --force \
Добавился RAID-массив md63 с одним диском \
![46]()\
Отображается в дереве lsblk новый RAID-массив на диске sdb \
![47]()\
В выводе команды pvs появился второй RAID \
![48]()
---
7. Увеличиваем размер Volume Group
![49]()
![50]()
![51]()
![52]()\
LV var, log, root находятся на старом диске (md0) \
![53]()
![54]()
---
8. Перемещение данных со старого диска на новый
![55]()
---
9. Просмотр изменений \
![56]()
![57]()
![58]()
![59]() \
После команды pvs видно, что для нового массива появился физический том. LV var, log, root находятся на новом диске \
![60]()
![61]()
---
10. Удаление старого диска из RAID-массива
![62]()
![63]()
---
11. Подключение новых дисков
![64]()
![65]()
---
12. Копирование таблицы разделов
![66]()
![67]()
---
13. Копирование /boot
![68]()
---
14. Изменение размера второго диска
![69]()
![70]()
![71]()
---
15. Добавление диска к текущему RAID-массиву
![72]()
![73]()
---
16. Расширение количества дисков
![74]()
![75]()
---
17. Изменение размера первого диска
![76]()
![77]()
![78]()
---
18. Расширение RAID
![79]()
---
19. Расширение размера PV
![80]()
![81]()
---
20. Создание RAID из дисков sdc и sdd
![82]()
![83]()
---
21. Создание нового PV
![84]()
![85]()
---
22. Перенос данных со старого раздела на новый
![86]()
![87]()
![88]()
![89]()
![90]()
---
23. Перемена разделов
![91]()
![92]()
---
24. Изменение /etc/fstab
![93]()
---
25. Выполнение проверок
![94]()
![95]()
