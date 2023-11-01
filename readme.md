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
<img src="Image 1.png" alt="Выберите операционую систему">




