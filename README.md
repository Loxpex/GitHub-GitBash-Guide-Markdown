# Шпаргалка-гайд: GitHub, GitBash, MarkDown

____

Небольшая шпаргалка для себя в будущем

____

____

## Навигация в GitBash

____

pwd (print working directory) - Узнать в какой директории находимся

cd ***имя директории*** (change directory) - Перейти в другую директорию

. (точка) - Ссылка на текущую папку

.. (две точки) - Ссылка на предыдущую папку

ls (list) - Показать список файлов и папок в текущей директории

ls -a (all) - Показать ВСЕ файлы и папки, включая скрытые

ls -l (large наверно) - Показывает более подробную информацию о файлах

____

**Флаги можно миксовать друг с другом, например -la**

____

rm ***Имя файла или директории*** (remove) - Удаляет файл или пустую папку

rm -r (recursieve) - Удаляет папку и ВСЕ что внутри нее

rm -f (force) - Удаляет папку без подтверждения на удаление

____

touch ***Имя файла*** (Прикоснуться ~тыкнуть~) - Создать ФАЙЛ

mkdir ***Имя директории*** (make directory) - Создать ДИРЕКТОРИЮ

____

cat ***Имя файла или директории*** (concatenate ~кот?~) - Выводит содержимое файла/файлов, может вывести последовательно несколько файлов

echo ***Имя файла*** (эхо походу) - Выводит ТЕКСТ в терминал или файл

____

cp ***Имя файла/директории*** (copy) - Копирует файл или директорию

mv ***Имя файла/директории*** (move) - Перемешает файл или директорию

clip < ***имя текстового файла*** (хз) - Скопировать в буфер обмена содержимое файла

____

____

## Команды Git 

____

Перед созданием удаленного репозитория на GitHub необходимо создать локальный репозиторий. 
Для этого используются следующие команды

git init (initialize) - Сделать папку, в которой была вызвана эта команда, Git репозиторием

Чтобы разгитить папку, нужно удалить скрытую папку .git 

git status - Вывести информацию о репозитории

git add ***Имя файла/папки*** - подготовить файл к сохранению

git add --all или . - Можно добавить в репозиторию всю текущую папку

git commit - Сохранить изменения

git commit -m (message) "*Комментарий*" - Сохранить изменения и добавить к ним комментарий

git log - Вывести список коммитов
____

Если написать просто git commit то откроется текстовый редактор который заставит написать комментарий.

Написать комментарий, нажать esc, написать :wq (write, quit)
____

____

## Работа с GitHub

Чтобы привзяать свой локальный репозиторй к удаленному, необходимо создать этот удаленный репозиторий на GitHub

Чтобы присоединить удаленный репоизторий к локальному, нужно создать SSH ключ, если такого нет.

____

### Генерация SSH ключа

____

ssh-keygen -t ed25519 -C "*электронная почта, к которой привязан GitHub*" 

Потом указать место в которое сохранить ключи

ed25519 - Алгоритм шифрования

Ключей 2 штуки. Один публичный, его можно показываеть. Другой секрет фирмы, его нельзя показывать.

____

В настройках своего профиля в GitHub добавьте свой публичный SSH ключ

ssh -T git@github.com - Если после ввода этой команды, и последующего подтверждения, GitHub нас приветствует, то аутентфикация прошла успешно

____

Чтобы привзяать локальный репозиторий к удаленному, перейдите в локальный репозиторий, и введите:

git remote add origin "*Ссылка на странцице репозитория в гитхабе, с типом SSH*" 

origin - псевдоним главного удаленного репозитория

git remote -v - Узнать все ли прошло успешно во время привзяки

____

git push -u origin main/master - ПЕРВЫЙ раз отправить изменения в удаленный репозиторий

-u Свяжет локальную ветку с одноименной удаленной

git push - дальше можно писать просто вот так

____

____

## Разметка MarkDown

____

"#" - Большой заголовок

"##" - Поменьше заголовок

и т.д

"----" - Полоска

Перенос текста на следующую строку - два энтера ! 

*Курсив* - * Слева и справа от текста

**Полужирный шрифт** - ** Слева и справа от текста

~~Зачеркнуть текст~~ - ~~ Слева и справа от текста

