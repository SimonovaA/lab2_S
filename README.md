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
![30](https://user-images.githubusercontent.com/50047846/58342309-e83c5280-7e58-11e9-93a5-7c6749281c64.png)
![31](https://user-images.githubusercontent.com/50047846/58342310-e8d4e900-7e58-11e9-8a6c-a43e97668cf0.png)
![32](https://user-images.githubusercontent.com/50047846/58342311-e8d4e900-7e58-11e9-8f81-9770689fd4ae.png)
![33](https://user-images.githubusercontent.com/50047846/58342313-e96d7f80-7e58-11e9-8061-3f0768041bc0.png)
---
2. Добавление нового диска ssd4, просмотр изменений
![34](https://user-images.githubusercontent.com/50047846/58342314-e96d7f80-7e58-11e9-9224-3a029b596c87.png)
![35](https://user-images.githubusercontent.com/50047846/58342315-e96d7f80-7e58-11e9-893f-9f382a8df6f7.png)
![36](https://user-images.githubusercontent.com/50047846/58342316-ea061600-7e58-11e9-9cf4-83326d9ea701.png)
---
3.  Копирование файловой таблицы со старого диска на новый
![37](https://user-images.githubusercontent.com/50047846/58342318-ea061600-7e58-11e9-9525-5fc08e7066be.png)
![39](https://user-images.githubusercontent.com/50047846/58342319-ea061600-7e58-11e9-835b-a09c26ebf63c.png)\
После выполнения команды sfdisk на новом диске (sdb) появились разделы sdb1 и sdb2.
![40](https://user-images.githubusercontent.com/50047846/58342320-ea061600-7e58-11e9-856b-cdaab653d776.png)
---
4. Скопировали данные /boot с sda1 на sdb1
---
5. Перемонтировали /boot на новый диск (sdb) и установили grub
![41](https://user-images.githubusercontent.com/50047846/58342322-ea9eac80-7e58-11e9-8e75-30e0dc495de5.png)
![42](https://user-images.githubusercontent.com/50047846/58342323-ea9eac80-7e58-11e9-8797-600c4fdaa507.png)\
Мы выполнили команду grub-install /dev/sdb, чтобы установить загрузчик группы на новый диск.
---
6. Создаем новый RAID-массив с включением только одного диска sdb
![45](https://user-images.githubusercontent.com/50047846/58342324-ea9eac80-7e58-11e9-9b6f-6efb462c8c14.png)\
Команда mdadm работает с ключом --force \
Добавился RAID-массив md63 с одним диском \
![46](https://user-images.githubusercontent.com/50047846/58342325-ea9eac80-7e58-11e9-8b59-aa8fc5d39fd4.png)\
Отображается в дереве lsblk новый RAID-массив на диске sdb \
![47](https://user-images.githubusercontent.com/50047846/58342326-eb374300-7e58-11e9-807f-291a9f447b31.png)\
В выводе команды pvs появился второй RAID \
![48](https://user-images.githubusercontent.com/50047846/58342327-eb374300-7e58-11e9-8754-df99136e8faa.png)
---
7. Увеличиваем размер Volume Group
![49](https://user-images.githubusercontent.com/50047846/58342328-eb374300-7e58-11e9-9235-c9f7f7453db1.png)
![50](https://user-images.githubusercontent.com/50047846/58342329-eb374300-7e58-11e9-984e-241b603e620d.png)
![51](https://user-images.githubusercontent.com/50047846/58342330-ebcfd980-7e58-11e9-9dec-25ae427de315.png)
![52](https://user-images.githubusercontent.com/50047846/58342332-ebcfd980-7e58-11e9-9169-17da0387afde.png)\
LV var, log, root находятся на старом диске (md0) \
![53](https://user-images.githubusercontent.com/50047846/58342333-ec687000-7e58-11e9-94a0-2f3f509a5e6e.png)
![54](https://user-images.githubusercontent.com/50047846/58342334-ec687000-7e58-11e9-8433-98a45c22bbeb.png)
---
8. Перемещение данных со старого диска на новый
![55](https://user-images.githubusercontent.com/50047846/58342336-ec687000-7e58-11e9-9499-84d57689476d.png)
---
9. Просмотр изменений \
![56](https://user-images.githubusercontent.com/50047846/58342337-ed010680-7e58-11e9-9546-b330ceb80137.png)
![57](https://user-images.githubusercontent.com/50047846/58342338-ed010680-7e58-11e9-8a48-ef28f1dadb5b.png)
![58](https://user-images.githubusercontent.com/50047846/58342339-ed999d00-7e58-11e9-93e4-9136b92d5ac7.png)
![59](https://user-images.githubusercontent.com/50047846/58342340-ed999d00-7e58-11e9-9497-4e49045283d2.png) \
После команды pvs видно, что для нового массива появился физический том. LV var, log, root находятся на новом диске \
![60](https://user-images.githubusercontent.com/50047846/58342341-ee323380-7e58-11e9-8aa9-12626cac1e1c.png)
![61](https://user-images.githubusercontent.com/50047846/58342342-ee323380-7e58-11e9-8548-e2b890f42253.png)
---
10. Удаление старого диска из RAID-массива
![62](https://user-images.githubusercontent.com/50047846/58342344-ee323380-7e58-11e9-9e3f-dde514a57c82.png)
![63](https://user-images.githubusercontent.com/50047846/58342345-ee323380-7e58-11e9-8cd2-608673507eb6.png)
---
11. Подключение новых дисков
![64](https://user-images.githubusercontent.com/50047846/58342346-eecaca00-7e58-11e9-9c87-7f1015f83ec8.png)
![65](https://user-images.githubusercontent.com/50047846/58342347-eecaca00-7e58-11e9-9fbf-4a245be1b2c5.png)
---
12. Копирование таблицы разделов
![66](https://user-images.githubusercontent.com/50047846/58342348-eecaca00-7e58-11e9-9c14-8af217386015.png)
![67](https://user-images.githubusercontent.com/50047846/58342349-ef636080-7e58-11e9-8aca-26b5a0618a68.png)
---
13. Копирование /boot
![68](https://user-images.githubusercontent.com/50047846/58342350-ef636080-7e58-11e9-8c17-5529c763ac61.png)
---
14. Изменение размера второго диска
![69](https://user-images.githubusercontent.com/50047846/58342351-ef636080-7e58-11e9-9b6a-ca7aedfaa107.png)
![70](https://user-images.githubusercontent.com/50047846/58342352-effbf700-7e58-11e9-837e-6bdb4e76d14f.png)
![71](https://user-images.githubusercontent.com/50047846/58342353-effbf700-7e58-11e9-8dbd-edb61d5485b0.png)
---
15. Добавление диска к текущему RAID-массиву
![72](https://user-images.githubusercontent.com/50047846/58342355-effbf700-7e58-11e9-81a5-dffd4f4b9a38.png)
![73](https://user-images.githubusercontent.com/50047846/58342357-f0948d80-7e58-11e9-9c50-1cff30c8f4a7.png)
---
16. Расширение количества дисков
![74](https://user-images.githubusercontent.com/50047846/58342361-f12d2400-7e58-11e9-9d3b-bfedf90bd60a.png)
![75](https://user-images.githubusercontent.com/50047846/58342362-f12d2400-7e58-11e9-814c-b1b13effbcad.png)
---
17. Изменение размера первого диска
![76](https://user-images.githubusercontent.com/50047846/58342363-f12d2400-7e58-11e9-992d-ae14db978f9e.png)
![77](https://user-images.githubusercontent.com/50047846/58342364-f12d2400-7e58-11e9-83ee-ce409c1984b8.png)
![78](https://user-images.githubusercontent.com/50047846/58342365-f1c5ba80-7e58-11e9-9790-375b2489bc35.png)
---
18. Расширение RAID
![79](https://user-images.githubusercontent.com/50047846/58342366-f1c5ba80-7e58-11e9-8f8b-525719152446.png)
---
19. Расширение размера PV
![80](https://user-images.githubusercontent.com/50047846/58342367-f1c5ba80-7e58-11e9-8215-985accba2e5b.png)
![81](https://user-images.githubusercontent.com/50047846/58342369-f25e5100-7e58-11e9-9a02-afc5f4dc67d7.png)
---
20. Создание RAID из дисков sdc и sdd
![82](https://user-images.githubusercontent.com/50047846/58342371-f25e5100-7e58-11e9-903f-9c62c920195f.png)
![83](https://user-images.githubusercontent.com/50047846/58342372-f2f6e780-7e58-11e9-98e5-05950cd1441b.png)
---
21. Создание нового PV
![84](https://user-images.githubusercontent.com/50047846/58342373-f2f6e780-7e58-11e9-81c9-10044d97c898.png)
![85](https://user-images.githubusercontent.com/50047846/58342375-f2f6e780-7e58-11e9-93a3-5f3c37a2cd7c.png)
---
22. Перенос данных со старого раздела на новый
![86](https://user-images.githubusercontent.com/50047846/58342391-f5594180-7e58-11e9-8bde-2f4b50017abd.png)
![87](https://user-images.githubusercontent.com/50047846/58342376-f38f7e00-7e58-11e9-85f4-b7780a72b59e.png)
![88](https://user-images.githubusercontent.com/50047846/58342379-f38f7e00-7e58-11e9-945d-7200379e27fb.png)
![89](https://user-images.githubusercontent.com/50047846/58342382-f4281480-7e58-11e9-8096-871cca110660.png)
![90](https://user-images.githubusercontent.com/50047846/58342383-f4281480-7e58-11e9-915a-b7c241dc1528.png)
---
23. Перемена разделов
![91](https://user-images.githubusercontent.com/50047846/58342384-f4281480-7e58-11e9-97a0-c9cd87c5b967.png)
![92](https://user-images.githubusercontent.com/50047846/58342386-f4281480-7e58-11e9-9024-6850cbb4fc8c.png)
---
24. Изменение /etc/fstab
![93](https://user-images.githubusercontent.com/50047846/58342387-f4c0ab00-7e58-11e9-817d-ec504f3ba16a.png)
---
25. Выполнение проверок
![94](https://user-images.githubusercontent.com/50047846/58342388-f4c0ab00-7e58-11e9-9297-e790bc895ef7.png)
![95](https://user-images.githubusercontent.com/50047846/58342389-f4c0ab00-7e58-11e9-841e-5a97e8a0ce60.png)
![96](https://user-images.githubusercontent.com/50047846/58342390-f4c0ab00-7e58-11e9-95ba-84754ed0ad57.png)
