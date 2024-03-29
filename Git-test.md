## Lesson 1
# инструкция по работе с Git
## Основные команды Git
**git help** - справка по командам  
**git init** - инициализация локального репозитория  
**git status** - получить информацию от git о его текущем состоянии  
**git add** - добавить версионность  
**git commit -m "коментарий"** - создание коммита  
**git log** - вывод на экран истории всех каммитов с их хеш-кодами  
**git checkout** - переход от одного каммита к другому  
**git checkout master** - вернуться к актуальному состоянию и продолжить работу  
**git diff** - увидеть разницу между текущим файлом и закоммиченным файлом  
## Удалённые репозитории
Пока что мы обсуждали использование Git только на локальной машине. Однако мы можем хранить историю коммитов удалённых репозиториев, которую можно отслеживать и обновлять. **git remote -v** выводит список удалённых репозиториев, которые мы отслеживаем, и имена, которые мы им присвоили.

При использовании команды **git clone <url репозитория>** мы не только загружаем себе копию репозитория, но и неявно отслеживаем удалённый сервер, который находится по указанному адресу и которому присваивается имя **origin**.

Наиболее употребляемые команды:
**it remote add <имя> <url>** — добавляет удалённый репозиторий с заданным именем  
**git remote remove <имя>**— удаляет удалённый репозиторий с заданным именем  
**git remote rename <старое имя> <новое имя>** — переименовывает удалённый репозиторий  
**git remote set-url <имя> <url>** — присваивает репозиторию с именем новый адрес  
**git remote show <имя>** — показывает информацию о репозитории  

## Следующие команды работают с удалёнными ветками:

**git fetch <имя> <ветка>** — получает данные из ветки заданного репозитория, но не сливает изменения  
**git pull <имя> <ветка>** — сливает данные из ветки заданного репозитория  
**git push <имя> <ветка>** — отправляет изменения в ветку заданного репозитория. Если локальная ветка уже отслеживает удалённую, то можно использовать просто **git push или git pull**  

![Gitlab logo](https://tproger.ru/signed_image/m-YXw3HiqvqHe75OdTlPSl-D9FR823NWNguJHLADB-Y/rs:fill:766:0:true/cb:vimg_2/f:webp/aHR0cHM6Ly9tZWRpYS50cHJvZ2VyLnJ1L3VwbG9hZHMvMjAxOS8wMi9wdXNoLXB1bGwuanBn)

## Работа с ветками

**git branch <имя ветки>** — создаёт новую ветку с HEAD, указывающим на HEAD. Если не передать аргумент <имя ветки>, то команда выведет список всех локальных веток  
**git checkout <имя ветки>** — переключается на эту ветку. Можно передать опцию **-b**, чтобы создать новую ветку перед переключением  
**git branch -d <имя ветки>** — удаляет ветку.  
Локальный и удалённый репозитории могут иметь немало ветвей, поэтому когда вы отслеживаете удалённый репозиторий — отслеживается удалённая ветка (git clone привязывает вашу ветку **master** к ветке **origin/master** удалённого репозитория).

## Привязка к удалённой ветке:

**git branch -u <имя удалённого репозитория>/<удалённая ветка>**— привязывает текущую ветку к указанной удалённой ветке  
**git checkout --track <имя удалённого репозитория>/<удалённая ветка>** — аналог предыдущей команды  
**git checkout -b <ветка> <имя удалённого репозитория>/<удалённая ветка>** — создаёт новую локальную ветку и начинает отслеживать удалённую  
**git branch --vv** — показывает локальные и отслеживаемые удалённые ветки  
**git checkout <удалённая ветка>** — создаёт локальную ветку с таким же именем, как у удалённой, и начинает её отслеживать.  
![Gitlab logo](https://tproger.ru/signed_image/-eEzSK69scn6FFR-URkKv8L_SBbccPjPdIYegfGrP4Y/rs:fill:766:0:true/cb:vimg_2/f:webp/aHR0cHM6Ly9tZWRpYS50cHJvZ2VyLnJ1L3VwbG9hZHMvMjAxOS8wMi9icmFuY2hpbmcuanBn)
**git status** - получить информацию от git о его текущем состоянии   
## Lesson 2
**git branch** - выводит ветки
**git branch name** - создание ветки
