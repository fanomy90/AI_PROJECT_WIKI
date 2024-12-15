# AI_PROJECT_WIKI
AI project Wikipedia
Настройка подключения к базе
1. Устанавливаем obsidian (https://obsidian.md/download) и устанавл
2. Устанавливаем github (https://git-scm.com/download/win) и настраиваем по инструкции https://publish.obsidian.md/git-doc/Installation
3. Установка `libsecret` и использование `git-credential-libsecret` запускаем установленное приложение запускаем git bash и выполняем команды: git config --global credential.helper libsecret  git config credential.helper (инструкция https://publish.obsidian.md/git-doc/Authentication)
4. Выполняем клонирование проекта из репозитория в папку где будет храниться хранилище Obsidian с помощью команды: git clone https://github.com/fanomy90/AI_PROJECT_WIKI.git "C:\VScode\AI\AI_PROJECT_WIKI" где https://github.com/fanomy90/AI_PROJECT_WIKI.git ссылка на репозиторий, "C:\VScode\AI\AI_PROJECT_WIKI" папка хранилища
5. Запускаем Obsidian и указываем папку которую клонировал git.
6. В программе слева внизу заходим в настройки (шестиренка) - Сторонние плагины и включаем возможность устанавливать сторонние плагины
7. В плагинах сообщетва ищем плагин: Git (Автор: Vinzent, (Denis Olehov) и включаем плагин
8. В настройках плагина нужно установить настройки автосинхронизации Auto commit-and-sync interval, включить Auto commit-and-sync after stopping file edits, в Commit message on auto commit-and-sync и Commit message on manual commit добавляем свой никнейм для разделения сообщений комитов, включаем Pull on startup
9. Настраиваем сочетания клавиш по примеру: Git: Commit all changes - Ctrl + стрелка вправо, Git: Commit-and-sync - Ctrl + стрелка влево, Git: Pull - Ctrl + стрелка вверх, Git: Push - Ctrl + стрелка вниз.
