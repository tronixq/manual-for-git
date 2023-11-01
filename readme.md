# **Инструкция  по Git  и Github**
## Основные команды  Git
### _Навигация_
pwd — покажи, в какой я папке <br>
ls-покажи файлы и папки в текущей папке<br>
ls -a— покажи также скрытые файлы и папки, названия которых начинаются с символа .<br>
cd new folder - перейди в папку <br>
cd new folder/folder 2 — перейди в папку folder2, которая находится в папке new folder <br>
cd ..перейди на уровень выше, в родительскую папку <br>
cd ~  перейди в домашнюю директорию (/Users/Username) <br>
cd /перейди в корневую директорию <br>
### _РАбота с файломи_
touch test.txt создай файл test.txt в текущей папке <br>
touch test.txt style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел <br>
mkdir new folder - создай папку с именем new folder в текущей папке <br>
### _Копирование и перемещение_
cp test.txt ~/my-dir — скопируй файл в другое место <br>
mv test.txt ~/my-dir — перемести файл или папку в другое место <br>
### _Чтение_
cat test.txt — распечатай содержимое текстового файла test.txt <br>
### _Удаление_
rm test.txt — удали файл test.txt <br>
rmdir folder2 — удали папку images <br>
rm -r new folder — удали папку new folder и всё, что она содержит <br>
### Полезные возможности
Команды необязательно печатать и выполнять по очереди. <br> Можно указать их списком — разделить двумя амперсандами (&&). <br>

У консоли есть собственная память — буфер с несколькими последними командами. <br> По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓). <br>

Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. <br> Если файл или папка есть в текущей директории, командная строка допишет путь сама. <br>
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. <br> Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. Останется только нажать Enter.
# **Установка командной строки <br> для пользователей Windows**
Командная строка — один из основных инструментов взаимодействия с компьютером. <br> Подробнее о ней мы расскажем в следующем уроке. <br> А пока вам может понадобиться выполнить подготовительные действия.
### _Инструкция по установке для пользователей Windows_
Windows поставляется с консолью — как и другие операционные системы. <br> Но при этом команды консоли Windows и macOS/Linux отличаются друг от друга. <br>
В повседневной работе большинство пользователей Git используют консоли с наборами команд, похожие на те, что применяют в macOS и Linux. <br>
Для этого нужно установить специальный консольный инструмент для Windows, <br> который называется Git Bash. <br>
Есть несколько способов установки. Мы рекомендуем пакет Git for Windows. <br> Он установит не только Bash, но и сам Git, который всё равно понадобится вам дальше. <br> Вот что нужно сделать:
1. Перейдите <a href="https://git-scm.com/download/win" target="_blank">на эту страницу официального сайта Git.</a> <br>
2. Скачайте одну из двух версий из категории Standalone Installer. Узнать тип вашей системы Windows можно в настройках.
3. Запустите программу установки. Обратите внимание, куда будет установлен Git. Обычно это директория C:\Program Files\Git. <br>
4. Проверьте, что в списке устанавливаемых программ стоит галочка напротив пункта Git Bash Here — это позволит открывать консоль с Git в любой папке. <br>
5. Далее установщик предложит много опций. Для нашего курса достаточно оставить все настройки по умолчанию. Несколько раз нажмите Next, пока не начнётся процесс установки.
6. После окончания установки нажмите Finish.
# Первый запуск Git Bash
Запустите программу Git Bash. Сделать это можно двумя способами. <br> Можно ввести название программы в окно поиска на панели задач. <br>
<br>
А можно открыть директорию, в которую был установлен Git. <br> Обычно это директория C:\Program Files\Git\bin. Перейдите в bin и запустите файл bash.exe. <br> 
Откроется консоль, в которой будет написано что-то похожее: USER_NAME@HOST_NAME MINGW64 ~ <br>
<br>
Вместо USER_NAME будет указано ваше имя пользователя, а вместо HOST_NAME — имя компьютера. <br> Если вы видите консоль, значит, установка прошла успешно. В нескольких следующих уроках покажем, как работать с ней.  <br>
<br>
Ура! Теперь на вашем компьютере есть не только командная строка, но и Git. <br> Устанавливать его вам уже не потребуется.
# Настройка Git 
Для настройки Git можно использовать командную строку. <br> Если у вас macOS или Linux, запустите программу Terminal. Если Windows — Git Bash.
## Работа с файлом настройки .gitconfig
Сейчас вы работаете в одиночку, но в дальнейшем вам может понадобиться использовать Git в команде. <br> Чтобы участникам проекта было понятно, кто и какие изменения вносил, нужно представиться и указать имя пользователя и адрес электронной почты. <br>
Вы можете указать любую электронную почту и любое имя. Сделать это можно с помощью команды git config  с ключом --global. <br>  При этом не имеет значения, в какой директории вы находитесь прямо сейчас: вызов git config --global сработает везде. <br>
В качестве значения user.name нужно указать своё имя или никнейм. Для настройки параметра user.email указывают электронную почту. <br>
``` $ git config --global user.name "User Namovich" 
# имя или ник нужно написать латиницей и в кавычках

$ git config --global user.email username@yandex.ru
# здесь нужно указать свой настоящий email ```