# Linux terminal - commands
1. Просмотреть где я - pwd
2. Создать папку - mkdir foldername
3. Зайти в папку - cd foldername
4. Создать 3 папки - mkdir foldername1 foldername2 foldername3
5. Зайти в любую папку - cd foldername1
6. Создать 5 файлов (3 txt, 2 json) - touch filename1.txt filename2.txt filename3.txt filename4.json filename5.json
7. Создать 3 папки - mkdir foldername4 foldername5 foldername6
8. Вывести список содержимого папки - ls -la 
9. Открыть любой txt файл - vim filename1.txt
10. Написать туда что-нибудь, любой текст - i
{	"group":27,
	"population":401,
	"men": "{	{"name":"Alex",
			"age":30}	
	}}

11. Cохранить и выйти - esc :wq
12. Выйти из папки на уовень выше - cd ..
13. Переместить любые 2 файла, которые вы создали, в любую другую папку - mv foldername1/{filename1.txt,filename2.txt} foldername1/foldername4
14. Скопировать любые 2 файла, которые вы создали, в любую другую папку - cp foldername1/{filename3.txt,filename4.json} foldername1/foldername5
16. Посмотреть содержимое в реальном времени (команда grep) - tail -f filename1.txt 
 -  Поиск конкретного значения при мониторинге файла - tail -f filename1.txt | grep
17. Вывести несколько первых строк из текстового файла - head -2 filename1.txt
18. Вывести несколько последних строк из текстового файла - tail -2 filename1.txt
19. Посмотреть содержимое длинного файла - less filename1.txt
20. Вывести дату и время - date

**Задание**
*********

1. Отправить http запрос на сервер

- http://162.55.220.72:5005/terminal-hw-request

curl "http://162.55.220.72:5005/terminal-hw-request"

{"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}

*Task 1*

curl "http://162.55.220.72:5005/get_method?name="ekaterina"&age=32"

["ekaterina","32"]

- http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000
curl "http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000"

2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
nano script.sh

#!/bin/bash

cd foldername

mkdir folderscript1 folderscript2 folderscript3

cd folderscript1

touch filescript1.txt filescript2.txt filescript3.txt filescript4.json filescript5.json

mkdir folderscript4 folderscript5 folderscript6

ls -la

mv {filescript1.txt,filescript2.txt} folderscript4  


chmod +x script.sh

./script.sh



