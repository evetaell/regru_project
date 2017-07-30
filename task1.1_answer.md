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

## 6.
$ git clone /home/evetaell/work/project1/ /home/evetaell/work/project13
Клонирование в «/home/evetaell/work/project13»…
готово.

## 7. 
Создала fileA и fileB. Изменила tast1.1_answer. 

git status
На ветке master
Ваша ветка обновлена в соответствии с «origin/master».
Изменения, которые будут включены в коммит:
  (используйте «git reset HEAD <файл>…», чтобы убрать из индекса)

	новый файл:    fileA.md
	новый файл:    fileB.md

Изменения, которые не в индексе для коммита:
  (используйте «git add <файл>…», чтобы добавить файл в индекс)
  (используйте «git checkout -- <файл>…», чтобы отменить изменения
   в рабочем каталоге)

	изменено:      task1.1_answer.md

git commit -m "Create fileA and fileB"

cd /home/evetaell/work/project1/
$ git pull project13 master

remote: Подсчет объектов: 4, готово.
remote: Сжатие объектов: 100% (2/2), готово.
remote: Total 4 (delta 0), reused 0 (delta 0)
Распаковка объектов: 100% (4/4), готово.
Из /home/evetaell/work/project13
 * branch            master     -> FETCH_HEAD
   fdc80f9..4553ce3  master     -> project13/master
Обновление fdc80f9..4553ce3
Fast-forward
 fileA.md | 1 +
 fileB.md | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 fileA.md
 create mode 100644 fileB.md

## 8.
git diff fileA.md
diff --git a/fileA.md b/fileA.md
index 0906b88..d3dce88 100644
--- a/fileA.md
+++ b/fileA.md
@@ -1 +1,2 @@
-String 1
\ No newline at end of file
+String 1
+String 2

git rm fileB.md
rm 'fileB.md'

$ git hist
* 56249b8 2017-07-30 | Change fileA, delete fileB (HEAD -> master) [Светлана Хмелева]
* 4553ce3 2017-07-30 | Create fileA and fileB (project13/master) [Светлана Хмелева]
* fdc80f9 2017-07-29 | Create file - task1.1_answer.md (ourPep/master) [Светлана Хмелева]

$ git push ourPep master
Username for 'https://github.com': evetaell
Password for 'https://evetaell@github.com': 
Подсчет объектов: 8, готово.
Delta compression using up to 4 threads.
Сжатие объектов: 100% (5/5), готово.
Запись объектов: 100% (8/8), 1001 bytes | 0 bytes/s, готово.
Total 8 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/evetaell/my_project.git
   fdc80f9..56e8fe9  master -> master

## 9.
во втором

git add . 
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git commit -m "Cgange task1.1_answer"
[master 5acedf1] Cgange task1.1_answer
 1 file changed, 78 insertions(+)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git log
commit 5acedf11918e976c5fd2348cfe3fdd0d215ad715
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 08:38:25 2017 +0400

    Cgange task1.1_answer

commit 4553ce38de751ea75a21252b5bd63f56ca56d800
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 00:27:17 2017 +0400

    Create fileA and fileB

commit fdc80f99e40e827edf189afdfc8e254383b043b7
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sat Jul 29 14:10:26 2017 +0400

    Create file - task1.1_answer.md

в первом
cd /home/evetaell/work/project1
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git hist
* 56e8fe9 2017-07-30 | Change fileA, delete fileB (HEAD -> master, ourPep/master) [Светлана Хмелева]
* 4553ce3 2017-07-30 | Create fileA and fileB (project13/master) [Светлана Хмелева]
* fdc80f9 2017-07-29 | Create file - task1.1_answer.md [Светлана Хмелева]

во втором фикс правок

cd /home/evetaell/work/project13/
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git commit --amend -m "Change task1.1_answer"
[master 6fc4de6] Change task1.1_answer
 Date: Sun Jul 30 08:38:25 2017 +0400
 1 file changed, 110 insertions(+)


лог первого
git hist
* 5e43829 2017-07-30 | Change task1.1_answer (HEAD) [Светлана Хмелева]
* 56e8fe9 2017-07-30 | Change fileA, delete fileB (ourPep/master) [Светлана Хмелева]
* 4553ce3 2017-07-30 | Create fileA and fileB [Светлана Хмелева]
* fdc80f9 2017-07-29 | Create file - task1.1_answer.md [Светлана Хмелева]
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ 

## 10.

git checkout 4553ce3 fileB.md

лог в первом

## 11.
git hist
* 8850748 2017-07-30 | FileB restore and change task1.1_answer (HEAD -> master) [Светлана Хмелева]
* 8921b44 2017-07-30 | Delete fileB, change task1.1_answer [Светлана Хмелева]
* f5f8668 2017-07-30 | Change fileA [Светлана Хмелева]
* dd9bd7b 2017-07-30 | Create fileA and fieB [Светлана Хмелева]
* 0495780 2017-07-30 | Create task1.1_answer.md [Светлана Хмелева]

лог во втором

git hist
* 8850748 2017-07-30 | FileB restore and change task1.1_answer (HEAD -> master, project1/master) [Светлана Хмелева]
* 8921b44 2017-07-30 | Delete fileB, change task1.1_answer [Светлана Хмелева]
* f5f8668 2017-07-30 | Change fileA [Светлана Хмелева]
* dd9bd7b 2017-07-30 | Create fileA and fieB [Светлана Хмелева]
* 0495780 2017-07-30 | Create task1.1_answer.md (origin/master, origin/HEAD) [Светлана Хмелева]

## 12.
git checkout -b feature1
Переключено на новую ветку «feature1»
$ git add .
$ git commit -m "New feature1 and change fileB and task1.1_answer"

## 13.
cd /home/evetaell/work/project13/
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git checkout -b feature2
Переключено на новую ветку «feature2»

## 14.
$ git pull origin feature1
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 1 (delta 0), pack-reused 0
Распаковка объектов: 100% (3/3), готово.
Из https://github.com/evetaell/regru_project
 * branch            feature1   -> FETCH_HEAD
 * [новая ветка]     feature1   -> origin/feature1
Обновление 8850748..91064fe
Fast-forward
 fileB.md          |  1 +
 task1.1_answer.md | 26 ++++++++++++++++++++++++++
 2 files changed, 27 insertions(+)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git co master
Переключено на ветку «master»
Ваша ветка опережает «origin/master» на 4 коммита.
  (используйте «git push», чтобы опубликовать ваши локальные коммиты)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git merge feature1
merge: feature1 — not something we can merge

Возможно, вы имели в виду это?
	origin/feature1
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git merge origin/feature1
Обновление 8850748..91064fe
Fast-forward
 fileB.md          |  1 +
 task1.1_answer.md | 26 ++++++++++++++++++++++++++
 2 files changed, 27 insertions(+)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ 

## 15.

git co feature2
Переключено на ветку «feature2»

git branch
* feature2
  master

git branch -a
* feature2
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/feature1
  remotes/origin/feature2
  remotes/origin/master
  remotes/project1/master  #ветка в первом репозитории

## 16.
откат до слияния с feature1

$ git co f952352
Note: checking out 'f952352'.

слияние master c feature2

$ git merge origin/feature2


## 17.

$git log --stat --graph
*   commit 6699a01241fdbe7a1944c091db3debd8797df1fb
|\  Merge: db252b5 0d14d6d
| | Author: Светлана Хмелева <hmeleva@reg.ru>
| | Date:   Sun Jul 30 16:24:54 2017 +0400
| | 
| |     Fix task1.1_answer
| |   
| * commit 0d14d6d326c625af4432cc48a3103e43c1c43a12
| | Author: Светлана Хмелева <hmeleva@reg.ru>
| | Date:   Sun Jul 30 15:59:19 2017 +0400
| | 
| |     Look branches and change task1.1_answer
| | 
| |  task1.1_answer.md | 58 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
| |  1 file changed, 58 insertions(+)
| |     
* |   commit db252b5e4d9a3a804ac67c198c03d5c8cb6b5d5e
|\ \  Merge: f952352 c964ae9
| | | Author: Светлана Хмелева <hmeleva@reg.ru>
| | | Date:   Sun Jul 30 16:15:03 2017 +0400
| | | 
| | |     Change task1.1_answer - fix conflict
| | |    
| * | commit c964ae99010ca919f9900e0d0ba499c1f72bcce5
| | | Author: Светлана Хмелева <hmeleva@reg.ru>
| | | Date:   Sun Jul 30 15:42:22 2017 +0400
| | | 
| | |     Change task1.1_answer
| | | 
| | |  task1.1_answer.md | 4 ----
| | |  1 file changed, 4 deletions(-)
| | |      
| * |   commit af61dff1284b440e712b8486e2681e638bcd2381
| |\ \  Merge: 30bcd56 7902470
| | | | Author: Светлана Хмелева <hmeleva@reg.ru>
| | | | Date:   Sun Jul 30 15:38:56 2017 +0400
| | | | 
| | | |     Merge branch 'master' of https://github.com/evetaell/regru_project
| | | |     
| * | | commit 30bcd567f4d8aae6d3e8cc18a58dd1e2f3c0e7bb
| | |/  Author: Светлана Хмелева <hmeleva@reg.ru>
| |/|   Date:   Sun Jul 30 15:35:18 2017 +0400
| | |   
| | |       Create feature2, merge feature1 in master and change task1.1_answer
| | |   
| | |    task1.1_answer.md | 36 ++++++++++++++++++++++++++++++++++++
| | |    1 file changed, 36 insertions(+)
| | |    
* | | commit f952352378de9b799e6dd113857a40c948cb0f4e
| |/  Author: Светлана Хмелева <hmeleva@reg.ru>
|/|   Date:   Sun Jul 30 16:13:26 2017 +0400
| |   
| |       Change task1.1_answer
| |   
| |    task1.1_answer.md | 58 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
| |    1 file changed, 58 insertions(+)
| |   
* | commit 79024708d001ed66331c9ab7a19222fe208f47f0
| | Author: Светлана Хмелева <hmeleva@reg.ru>
| | Date:   Sun Jul 30 15:25:25 2017 +0400
| | 
| |     Change fileB
| | 
| |  fileB.md | 1 +
| |  1 file changed, 1 insertion(+)
| |     
* |   commit b4f003bd774f39a601f288d79c197a2f2118226a
|\ \  Merge: 91064fe 29ffdd9
| |/  Author: Светлана Хмелева <hmeleva@reg.ru>
|/|   Date:   Sun Jul 30 15:18:35 2017 +0400
| |   
| |       Fix conflict
| |   
| * commit 29ffdd966c70e046051268fa3c354e737f39e687
| | Author: Светлана Хмелева <hmeleva@reg.ru>
| | Date:   Sun Jul 30 14:38:30 2017 +0400
| | 
| |     FileB restore
| | 
| |  fileB.md | 1 +
| |  1 file changed, 1 insertion(+)
| |   
* | commit 91064fe941ae5e086eca7352a6ab5f3f20282aa2
| | Author: Светлана Хмелева <hmeleva@reg.ru>
| | Date:   Sun Jul 30 14:58:03 2017 +0400
| | 
| |     New feature1 and change fileB and task1.1_answer
| | 
| |  fileB.md          |  1 +
| |  task1.1_answer.md | 26 ++++++++++++++++++++++++++
| |  2 files changed, 27 insertions(+)
| |   
* | commit 885074808a8eefa947c9fe4b0f323ab805d6757a
|/  Author: Светлана Хмелева <hmeleva@reg.ru>
|   Date:   Sun Jul 30 14:38:30 2017 +0400
|   
|       FileB restore and change task1.1_answer
|   
|    fileB.md          |   1 +
|    task1.1_answer.md | 154 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-------------------------
|    2 files changed, 118 insertions(+), 37 deletions(-)
|  
* commit 8921b44e5bdbe985ad475b90934c01c03b7abcf6
| Author: Светлана Хмелева <hmeleva@reg.ru>
| Date:   Sun Jul 30 13:59:04 2017 +0400
| 
|     Delete fileB, change task1.1_answer
| 
|  fileB.md          |  1 -
|  task1.1_answer.md | 37 +++++++++++++++++++++++++++++++++++++
|  2 files changed, 37 insertions(+), 1 deletion(-)
|  
* commit f5f866813c970975cb36341e702fcd7cf80659ee
| Author: Светлана Хмелева <hmeleva@reg.ru>
| Date:   Sun Jul 30 13:52:23 2017 +0400
| 
|     Change fileA
| 
|  fileA.md | 1 +
|  1 file changed, 1 insertion(+)
|  
* commit dd9bd7ba5a4fcf6a48fafc472f6ef737cdc9535b
| Author: Светлана Хмелева <hmeleva@reg.ru>
| Date:   Sun Jul 30 13:38:32 2017 +0400
| 
|     Create fileA and fieB
| 
|  fileA.md          |  1 +
|  fileB.md          |  1 +
|  task1.1_answer.md | 13 ++++++++++++-
|  3 files changed, 14 insertions(+), 1 deletion(-)
|  
* commit 0495780dd6efaa759ce328db7a9304759dee1dca
  Author: Светлана Хмелева <hmeleva@reg.ru>
  Date:   Sun Jul 30 10:57:13 2017 +0400
  
      Create task1.1_answer.md
  
   task1.1_answer.md | 77 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   1 file changed, 77 insertions(+)
(END)

$git branch -D feature1
Ветка feature1 удалена (была 91064fe).

$ git push origin :feature1
Username for 'https://github.com': evetaell
Password for 'https://evetaell@github.com': 
To https://github.com/evetaell/regru_project.git
 - [deleted]         feature1

## 18.

git tag v1.0

# 19 Репозитории синхронизированы

# 20 ссылка будет отправлена на mentors-team@dev.reg.ru 

