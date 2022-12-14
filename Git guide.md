# Инструкция по работе с Git
Чтобы начать работу с Git, для начала нам нужно выбрать папку в интерфейсе программы Visual Studio code.

Для это, пожалуйста, нажмите на опцию **Файл** и воспользуйтесь опцией открыть папку.

![Как открыть папку](pictures/0.png)

*Открыть папку можно и с помощью команды ctrl + k o*

После того, как мы открыли папку, нужно создать файл. Файл можно создать с любым расширением, но для сегодняшней инструкции мы будем использовать разрешение .md

![Как создать файл](pictures/1.png)

Для работы с Git, нам нужно открыть терминал, для этого выбираем опцию **Терминал** и нажимаем кнопку **Создать терминал**

![Как открыть терминал](Pictures/2.png)

## Для начала работы с Git нужно сделать следующее 
1. Нужно ввести команду git init
2. Нам нужно представиться программе, для этого используем следующие комманды

git config --global user.email "you@example.com"  

git config --global user.name "Your Name"

3. Добавить файл в репозиторий - git add "file_name"
4. И нажать ctrl + s, либо воспользоваться опцией **Файл** и нажать кнопку **сохранить**

После этого можно воспользоваться командой Git status. Если Вы все сделали верно, то Вы программа выведет следующий текст. 

![Гит статус](Pictures/4.png)

Т.к. у нас блок называется ***Контроль Версий***, то мы рассмотрим еще одну полезную функцию для работы с Git.

Что такое контроль версий? Ну это можно узнать на семинаре. 

#### Почему Git и ему подобные программы хороши для работы с контролем версий? Git хранит сумму разности от файла прошлой версии. Пример:
1. Вы пишите код для игры. Пускай Вам нужно прописать логику поведение отдельного НПС
2. Каждое его действие Вы отдельно сохраняете.
3. Случилось такое, что в поведении Вашего НПС произошла ошибка. Не будет вдаваться в подробности, нам нужно ее починить. 
#### Тут нам на помощь приходит Git. С его помощью мы можем откатиться на более раннюю версию кода и посмотреть,в какой из версий произошла данная ошибка.

Чтобы сохранить любые внесенные изменения, нужно воспользоваться командой Git commit -m "Что меняли/что добавили и тд"

Для одновременного добавления и сохранения можно использовать команду git commit -am ""

![Коммит](Pictures/5.png)

Теперь у нас есть своеобразное сохранение. Точка возврата. 

#### Введя команду Git Log ,мы увидим точку сохранения наших изменений.

![Коммит](Pictures/6.png)

Для того, чтобы откатить изменения к прошлой версии, можно воспользоваться командой git checkout "Первые 4 символа нашей точки сохранения после commit" 

![Перед возвратом](Pictures/7.png)
![Чекаут](Pictures/8.png)
![Что получилось](Pictures/9.png)

### 
Если вы хотите вернуть все как было, то можете использовать команду git checkout master

![Чекаут](Pictures/10.png)

Тут мы заканчиваем про работу с Git. Ибо работу с локальным репозиторием мы еще не изучали :)

## Язык разметки - Markdown.
С помощью данного языка можно стилизировать текст. Проще говоря, сделать текст читаемым и удобным. 

### Начнем с манипуляций с самим текстом.
Заголовки - их всегда нужно начинать с новой строки. Чтобы сделать заголовок, достаточно добавить символ "#" и написать текст через пробел. Чтобы уменить размер заголовка, достаточно добавить еще один или несколько символов "#". Самый большой заголовок #, а самый маленький ######.

## Для выделения текста можно воспользоваться следующими символами:
1. *Текст курсивом* * *
2. **Жирный текст** ** **
3. ***Жирный с курсивом*** *** ***
4. ~~Зачеркнутый~~ ~~ ~~
5. > цитирование >

Если Вы не хотите, чтобы markdown использовал символы, то их нужно перекрыть обратным слэшем - \*\*Не жирный\*\* 

## Составление списков.
Списки могут быть:

Макрикрованными
* Один
* Два
* Три

Нумированными 
1. Один
2. ДВа
3. Три

## С помощью Markdown можно вставлять картинки и ссылки.

Для картинок - ![Если не откроется картинка, будет этот текст](Папка/изображение\)

Для ссылок - ![Если не откроется картинка, будет этот текст](URL_ссылки_на_изображение "необязательный текст при наведении мыши"\)

# Работа с ветками

### Команды для работы с ветками

Для работы с ветками мы будем использовать следующую комманду git branch. При вводе этой команды в консоль, она покажет все доступные ветки. Чтобы создать новую ветку, нужно использовать команду git branch "название ветки". Переключение между ветками осуществляется через команду git checkout "название ветки".

### Объединение веток

Для объединения ячеек мы будем использовать данную команду - git merge “название ветки”

### Удаление веток

Для удаления веток мы будем использовать эту команду  git branch -d “название ветки”

### Конфликт

Эта строка нужна нам для конфликта.


# Работа с удаленным репозиторием

### Команды для работы с удаленным репозиторием

Чтобы скачать удаленный репозиторий, можно воспользоваться командой git clone [ссылка]

Чтобы загрузить свой репозиторий, нам нужно получить ссылку на хабе и воспользоваться командой git remote add (название)[ссылка]


### Отправление и изменений в репозиторий

Для подгрузки своих наработок и изменений, можно воспользоваться командой git push 

### Загрузка изменений

А для загрузки  изменений мы будем использовать команду git pull

Для изменения имени удаленного репозитория можно воспользоваться командой git remote rename имя

