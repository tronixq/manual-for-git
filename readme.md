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
Вы можете указать любую электронную почту и любое имя. Сделать это можно с помощью команды **git config  с ключом --global**. <br>  При этом не имеет значения, в какой директории вы находитесь прямо сейчас: вызов **git config --global** сработает везде. <br>
В качестве значения user.name нужно указать своё имя или никнейм. Для настройки параметра **user.email** указывают электронную почту. <br>

```
$ git config --global user.name "User Namovich" 
# имя или ник нужно написать латиницей и в кавычках

$ git config --global user.email username@yandex.ru

# здесь нужно указать свой настоящий email
```
Все глобальные настройки Git хранит в файле **.gitconfig** в домашней директории. <br> Команда запишет в этот файл указанные имя и почту. Чтобы убедиться в этом, можно вызвать команду для чтения файлов.

```
$ cat ~/.gitconfig
```
Другой способ проверки — вывести содержимое файла конфигурации Git той же командой **git config** с флагом **--list**.
```
$ git config --list
```
В ответ командная строка покажет текущие значения настроек.
```
user.name=Username
user.email=username@yandex.ru
```
**Готово!**
# Хеш — идентификатор коммита
В процессе работы с Git вам будет часто встречаться понятие «хеш коммита». <br> Эти странные строчки с бессмысленным (на первый взгляд) набором букв и цифр вы <br> могли видеть, когда вызывали команду git log и выводили историю коммитов.
## Что такое хеш. Хеширование коммитов
Хеширование  — это способ преобразовать набор данных и получить их «отпечаток»
Информация о коммите — это набор данных: когда был сделан коммит, <br> содержимое файлов в репозитории на момент коммита и ссылка на предыдущий, <br> или родительский, коммит.
Git хеширует (преобразует) информацию о коммите с помощью алгоритма SHA-1 <br> и получает для каждого коммита свой уникальный хеш — результат хеширования.
Обычно хеш — это короткая (40 символов в случае SHA-1) строка, которая состоит <br> из цифр 0—9 и латинских букв A—F (неважно, заглавных или строчных). <br> Она обладает следующими важными свойствами: <br>
если хеш получить дважды для одного и того же набора входных данных, то результат будет гарантированно одинаковый; <br>
если хоть что-то в исходных данных поменяется (хотя бы один символ), то хеш тоже изменится (причём сильно). <br>
Чтобы убедиться в этом, можно поэкспериментировать с SHA-1 <a href="https://emn178.github.io/online-tools/sha1.html" target="_blank"> на этом сайте — </a>  попробуйте ввести в поле input (англ. «ввод») разные символы, слова или предложения и понаблюдайте, как меняется хеш в поле output (англ. «вывод»).
# Хеш — основной идентификатор коммита
Git хранит таблицу соответствий хеш → информация о коммите. Если вы знаете хеш, <br> вы можете узнать всё остальное: автора и дату коммита и содержимое <br> закоммиченных файлов. Можно сказать, что хеш — основной идентификатор коммита.
При работе с Git хеши будут встречаться вам регулярно. Их можно будет <br> передавать в качестве параметра разным Git-командам, чтобы указать, <br> с каким коммитом нужно произвести то или иное действие.
Все хеши и таблицу хеш → информация о коммите Git сохраняет в служебные файлы. <br> Они находятся в скрытой папке .git в репозитории проекта.
# Исследуем лог
Дальше рассмотрим подробнее, из каких элементов состоит описание коммита, а также как вывести сокращённый лог. <br> Сокращённый лог полезен, если нужно быстро найти нужный коммит <br> среди сотни других.
## Элементы описания коммита
После вызова git log появляется список коммитов. <br>
### Разберём элементы, из которых состоит описание:
строка из цифр и латинских букв после слова commit — это хеш коммита; <br>
Author — имя автора и его электронная почта; <br>
Date — дата и время создания коммита; <br>
в конце находится сообщение коммита. <br>
Исходный код самого Git тоже хранится в Git-репозитории. <br> Вот так выглядит описание самого первого коммита в репозитории Git. Изучите его. <br>
```
commit e83c5163316f89bfbde7d9ab23ca2e25604af290
Author: Linus Torvalds <torvalds@linux-foundation.org>
Date:   Thu Apr 7 15:13:13 2005 -0700

    Initial revision of "git", the information manager from hell

```
# Сокращённый лог — git log --oneline
Получить сокращённый лог можно с помощью команды git log с флагом --oneline. <br> В терминале появятся только первые несколько символов <br> хеша каждого коммита и их комментарии.
Сокращённый лог полезен, если в репозитории уже много коммитов — например, <br> сотни или тысячи. В этом случае можно быстро найти нужный по описанию. <br>

Сокращённый хеш  можно использовать точно так же, как и полный. Для этого команда git log --oneline <br> автоматически подбирает такую длину сокращённых хешей, чтобы они были <br> уникальными в пределах репозитория и Git всегда мог понять, о каком коммите идёт речь.
# HEAD 
При вызове команды git log вы также могли заметить надпись (HEAD -> master) <br> после хеша одного из коммитов.
 ## Файл HEAD
 Файл HEAD  — один из служебных файлов папки <br> .git. Он указывает на коммит, который сделан последним (то есть на самый новый). <br>
 В этом можно убедиться с помощью терминала. Перейдите в папку .git <br> командой cd. Посмотрите содержимое файла HEAD командой cat. <br>
Внутри HEAD — ссылка на служебный файл: refs/heads/master <br> (или refs/heads/main в зависимости от названия ветки). Если заглянуть в этот файл, <br> можно увидеть хеш последнего коммита. <br>
Когда вы делаете коммит, Git обновляет refs/heads/master — записывает в него хеш последнего коммита. <br> Получается, что HEAD тоже обновляется, так как <br> ссылается на refs/heads/master. <br>
При работе с Git указатель HEAD используется довольно часто. <br> Мы уже упоминали, что многие команды Git принимают в качестве параметра хеш коммита. <br> Если нужно передать последний коммит, то вместо его хеша можно просто написать слово HEAD — Git поймёт, <br> что вы имели в виду последний коммит.
# Статусы файлов в Git
До появления Git системы контроля версий выделяли только два статуса у  файлов: «уже закоммичен» и «ещё не закоммичен». <br> Например, в Subversion (самой популярной VCS до эпохи Git) <br> не нужно было выполнять команду — аналог git add, а можно было просто сделать коммит (svn commit). <br> Эта команда по умолчанию добавляла в коммит все новые и изменённые файлы. <br>
Такое поведение интуитивно более понятно. Зато Git даёт больше контроля за состоянием файлов. <br> Хотя сначала это может показаться сложным, <br> со временем вы оцените удобство более явного подхода.
# Статусы untracked/tracked, staged и modified
Одна из ключевых задач Git — отслеживать изменения файлов в репозитории. <br> Для этого каждый файл помечается каким-либо статусом. Рассмотрим основные. <br>
Мы говорили, что новые файлы в Git-репозитории помечаются как untracked, то есть неотслеживаемые. <br> Git «видит», что такой файл существует, но не следит за изменениями в нём. <br> У untracked-файла нет предыдущих версий, зафиксированных в коммитах или через команду git add. <br>
После выполнения команды git add файл попадает в staging area, <br> то есть в список файлов, которые войдут в коммит. <br> В этот момент файл находится в состоянии staged. <br>
Состояние tracked — это противоположность untracked. <br> Оно довольно широкое по смыслу: в него попадают файлы, <br> которые уже были зафиксированы с помощью git commit, а также файлы, <br> которые были добавлены в staging area командой git add. <br> То есть все файлы, в которых Git так или иначе отслеживает изменения. <br>
Состояние modified означает, что Git сравнил содержимое файла с <br> последней сохранённой версией и нашёл отличия. <br> Например, файл был закоммичен и после этого изменён. <br>
# Про staged и modified
Команда git add добавляет в staging area только текущее содержимое файла. <br> Если вы, например, сделаете git add file.txt, а затем измените file.txt, то <br> новое содержимое файла не будет находиться в staging. <br>
Git сообщит об этом с помощью статуса modified: файл изменён относительно <br> той версии, которая уже в staging. Чтобы добавить в staging последнюю версию, <br> нужно выполнить git add file.txt ещё раз. <br>
# Оформление сообщений к коммитам
То, как написаны сообщения коммитов, тоже может подчиняться определённым правилам. <br> Иногда эти правила продиктованы культурой команды, а иногда техническими ограничениями. <br>
Например, в выводе команды git log --oneline умещается максимум 72 первых <br> символа сообщения, поэтому многие правила включают пункт: <br> «Сообщение не должно быть длиннее 72 символов». <br>
# Зачем вообще писать сообщения
У каждого коммита в Git есть сообщение — то, что передаётся после параметра -m. <br> Например: git commit -m "Добавить урок про оформление сообщений коммитов". <br>
Есть общие рекомендации по тому, как правильно составить сообщение. Оно должно быть: <br>
1. относительно коротким, чтобы его было легко прочитать; <br>
2. информативным. <br>
Вот пример полезного сообщения в репозитории новостного сайта: <br> Исправление опечатки в заголовке главной страницы на хорватском. Такое сообщение даёт много  информации: <br>
Исправление опечатки значит, что исправлена ошибка, которая была допущена при наборе. <br> Такое исправление не меняет смысл. То есть, например, <br> главному редактору не нужно перепроверять этот заголовок. <br>
На хорватском говорит о том, что переводчикам на другие языки этот <br> коммит можно смело пропускать. <br>
В заголовке главной страницы указывает, где произошли изменения. <br> Если, например, кто-то зайдёт на сайт и ему не понравится новый заголовок, <br> он легко найдёт по истории (git log) автора этого коммита и спросит у него, почему заголовок теперь такой. <br>