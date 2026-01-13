# gitCommands

1 путь
git init
git add platformio.ini src/ data/
git commit -m "Initial commit: only src, data, and platformio.ini"


2 путь----------------------------------------
# Убедитесь, что старый .git удалён (уже сделано)
rm -Recurse -Force .git

# Инициализация нового репозитория
git init

# Создание .gitignore (можно создать вручную или через echo)
echo @"
*
!platformio.ini
!src/
!src/**
!data/
!data/**
"@ | Out-File -Encoding utf8 .gitignore

# Добавление нужных файлов
git add platformio.ini src/ data/

# Первый коммит
git commit -m "создал папку data там html, веб сервер на sockets"

-------------------------------------------------
# (опционально) добавить .gitignore
git add .gitignore
git commit -m "add .gitignore"

-------------------------------------------------


3 путь
✅ Правильный способ удалить .git в PowerShell:

Remove-Item -Recurse -Force .git
Или сокращённо:
rm -Recurse -Force .git

git ls-files

# Игнорировать всё по умолчанию
*

# Но явно разрешить нужные файлы и папки
!platformio.ini
!src/
!src/**
!data/
!data/**

git add platformio.ini src/ data/

git commit -m "создал папку data там html, веб сервер на sockets"


