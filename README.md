# GitBash
## HW_1. The first part
### Linux terminal (GitBash) commands

1) Посмотреть где я 
 
`pwd`

2) Создать папку 

`mkdir group_30`

3) Зайти в папку 

`cd group_30`

4) Создать 3 папки 

`mkdir qa_1 qa_2 qa_3`

5) Зайти в любоую папку 

`cd qa_1`

6) Создать 5 файлов (3 txt, 2 json) 

`touch qq1.txt qq2.txt qq3.txt qq4.json qq5.json`

7) Создать 3 папки 

`mkdir qa_4 qa_5 qa_6`

8) Вывести список содержимого папки 

`ls -la`

9) + Открыть любой txt файл 

`vim qq1.txt`

10) + написать туда что-нибудь, любой текст. 

```
(*Нажимаем* _"i"_ ,*вводим текст*:)

name
surname
age
email
tel
```

11) + сохранить и выйти. 


`*Нажимаем* _"Esc"_ , *далее* _:wq "Enter"_`

12) Выйти из папки на уровень выше 

`cd ..`

13) переместить любые 2 файла, которые вы создали, в любую другую папку. 

`mv qa_1/{qq2.txt,qq3.txt} qa_3`

14) скопировать любые 2 файла, которые вы создали, в любую другую папку. 

`cp qa_1/{qq4.json,qq5.json} qa_2`

15) Найти файл по имени 

`find -name qq2.txt`

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает. 

`tail -f qa_1/qq1.txt`

17) вывести несколько первых строк из текстового файла 

`head -2 qa_1/qq1.txt`

18) вывести несколько последних строк из текстового файла 

`tail -n 2 qa_1/qq1.txt`

19) просмотреть содержимое длинного файла (команда less) изучите как она работает. 

`less qa_1/qq1.txt *(чтобы выйти* -_"q"_ *)*`

20) вывести дату и время 

`date`

##Задание *
1) Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request  

```
curl http://162.55.220.72:5005/terminal-hw-request
curl http://162.55.220.72:5005/get_method?name=Vika\&age=31
```

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

```
cat >> myscript.sh
#!/bin/bash
cd group_30
mkdir qa_7 qa_8 qa_9
cd qa_7
touch q11.txt q22.txt q33.txt q44.json q55.json
mkdir qa1 qa2 qa3
ls -la
mv {q11.txt,q22.txt} /e/qa/group_30/qa_8

*(после* _Ctrl+C_
chmod +x ./myscript.sh
./myscript.sh *)*
