# Ответы на упражнения

## 1. 

Создала в директории /home/evetaell/work каталог project1

$ cd /home/evetaell/work/project1
$ git init

## 2. 
$ git config --global user.name "Светлана Хмелева"
$ git config --global user.email hmeleva@reg.ru

$git config --list

user.name=Светлана Хмелева
user.email=hmeleva@reg.ru
core.autocrlf=input
core.safecrlf=true
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
alias.co=checkout
alias.ci=commit
alias.st=status
alias.br=branch
alias.hist=log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
alias.type=cat-file -t
alias.dump=cat-file -p
remote.ourPep.url=https://github.com/evetaell/my_project.git
remote.ourPep.fetch=+refs/heads/*:refs/remotes/ourPep/*

## 3. 
1. Зарегистрировалась на гитхаб
2. Создала новый проект
3. git remote add ourPep https://github.com/evetaell/my_project.git
4. git remote -v
   * ourPep	https://github.com/evetaell/my_project.git (fetch)
   * ourPep	https://github.com/evetaell/my_project.git (push)
5. git push ourPep master

## 4. 

Создала в репозитории файл task1.1.md, скопировала в него текст этого задания.

$git status

На ветке master
Начальный коммит
Неотслеживаемые файлы:
  (используйте «git add <файл>…», чтобы добавить в то, что будет включено в коммит)
	task1.1.md

Создала файл .gitignore, внесла туда task1.1.md

$git status

На ветке master
Начальный коммит

## 5. 

Создала в репозитории файл task1.1_answer.md, внесла все выполненные задания.

evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git commit -m "Create file - task1.1_answer.md"[master (корневой коммит) ca52e25] Create file - task1.1_answer.md
 1 file changed, 65 insertions(+)
 create mode 100644 task1.1_answer.md
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git status
На ветке master
нечего коммитить, нет изменений в рабочем каталоге

git push origin

## 6.
 git clone /home/evetaell/work/project1 project13
Клонирование в «project13»…
готово.

## 7.
Создала fileA и fileB, внесла правки в task1.1_answer. 
Сделала commit
Внесла task1.1_answer в игнор, чтобы его правки не попали в первый репозиторий.
Зашла в первый репозиторий

git pull project13 master

## 8. 
git add .
$ git commit -m "Change fileA"
[master f5f8668] Change fileA
 1 file changed, 1 insertion(+)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git log -p fileA.md
commit f5f866813c970975cb36341e702fcd7cf80659ee
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 13:52:23 2017 +0400

    Change fileA

diff --git a/fileA.md b/fileA.md
index 18a1a7a..d3dce88 100644
--- a/fileA.md
+++ b/fileA.md
@@ -1 +1,2 @@
 String 1
+String 2

commit dd9bd7ba5a4fcf6a48fafc472f6ef737cdc9535b
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 13:38:32 2017 +0400

    Create fileA and fieB

diff --git a/fileA.md b/fileA.md
new file mode 100644
index 0000000..18a1a7a
--- /dev/null
+++ b/fileA.md
@@ -0,0 +1 @@
+String 1
$ git rm fileB.md
rm 'fileB.md'

