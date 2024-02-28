Git Workflow Case Study

Question ?
You work as a Devops Architect in Zendriix Softwares. The company has been struggling to 
manage their product releases. The releases should happen on 25th of every month. Suggest a 
Git Workflow Architecture for this requirement. 
Simulate this workflow, by creating a pseudo code files and branches, and upload the same to 
your GitHub Account. 
As a part of solution, share the link to your GitHub repository. 

santh@Santhana MINGW64 /c
$ pwd
/c

santh@Santhana MINGW64 /c
$ mkdir GitWorkflowCaseStudy

santh@Santhana MINGW64 /c
$ cd GitWorkflowCaseStudy

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy
$ sudo git init
bash: sudo: command not found

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy
$ git init
Initialized empty Git repository in C:/GitWorkflowCaseStudy/.git/

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ nano master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git add .
warning: in the working copy of 'master.txt', LF will be replaced by CRLF the next time Git touches it

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git commit -m "Initial master.txt"
[main (root-commit) 801aba7] Initial master.txt
 1 file changed, 1 insertion(+)
 create mode 100644 master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch feature1

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch feature2

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch develop

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch release

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch
  develop
  feature1
  feature2
* main
  release

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git checkout feature1
Switched to branch 'feature1'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ nano feature1.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ nano feature1.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git add .
warning: in the working copy of 'feature1.txt', LF will be replaced by CRLF the next time Git touches it

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git commit -m "Adding feature1.txt to feature1"
[feature1 8bcdb4f] Adding feature1.txt to feature1
 1 file changed, 1 insertion(+)
 create mode 100644 feature1.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git checkout feature2
Switched to branch 'feature2'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature2)
$ nano feature2.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature2)
$ git add .
warning: in the working copy of 'feature2.txt', LF will be replaced by CRLF the next time Git touches it

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature2)
$ git commit -m "Adding feature2.txt to feature2"
[feature2 9c719d0] Adding feature2.txt to feature2
 1 file changed, 1 insertion(+)
 create mode 100644 feature2.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature2)
$ git checkout develop
Switched to branch 'develop'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ ls
master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ cat master.txt
This is master code for Case Study

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ git merge feature1
Updating 801aba7..8bcdb4f
Fast-forward
 feature1.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature1.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ git merge feature2
Merge made by the 'ort' strategy.
 feature2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature2.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ git checkout feature1
Switched to branch 'feature1'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ nano feature1.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ cat feature1.txt
This is feature1 for Case Study
Error Fixed

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git add .

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git commit -m "Error fixed in feature1"
[feature1 fc7e3c6] Error fixed in feature1
 1 file changed, 1 insertion(+)

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ cat feature1.txt
This is feature1 for Case Study
Error Fixed

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (feature1)
$ git checkout develop
Switched to branch 'develop'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ ls
feature1.txt  feature2.txt  master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ cat feature1.txt
This is feature1 for Case Study

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ git merge feature1
Merge made by the 'ort' strategy.
 feature1.txt | 1 +
 1 file changed, 1 insertion(+)

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ cat feature1.txt
This is feature1 for Case Study
Error Fixed

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (develop)
$ git checkout release
Switched to branch 'release'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (release)
$ git merge develop
Updating 801aba7..9c0f1d5
Fast-forward
 feature1.txt | 2 ++
 feature2.txt | 1 +
 2 files changed, 3 insertions(+)
 create mode 100644 feature1.txt
 create mode 100644 feature2.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (release)
$ git checkout main
Switched to branch 'main'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git merge release
Updating 801aba7..9c0f1d5
Fast-forward
 feature1.txt | 2 ++
 feature2.txt | 1 +
 2 files changed, 3 insertions(+)
 create mode 100644 feature1.txt
 create mode 100644 feature2.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ ls
feature1.txt  feature2.txt  master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git remote add origin https://github.com/Santhanakumar58/GitworkflowCaseStudy.git

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git push origin --all
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (16/16), 1.47 KiB | 1.47 MiB/s, done.
Total 16 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Santhanakumar58/GitWorkflowCaseStudy.git
To https://github.com/Santhanakumar58/GitworkflowCaseStudy.git
 * [new branch]      develop -> develop
 * [new branch]      feature1 -> feature1
 * [new branch]      feature2 -> feature2
 * [new branch]      main -> main
 * [new branch]      release -> release

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git push origin --tags
Everything up-to-date

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch
  develop
  feature1
  feature2
* main
  release

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch hotfix

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git checkout hotfix
Switched to branch 'hotfix'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ ls
feature1.txt  feature2.txt  master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ nano urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ git add .
warning: in the working copy of 'urgent.txt', LF will be replaced by CRLF the next time Git touches it

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ git commit -m "Adding urgent.txt from Hotfix"
[hotfix cd82b93] Adding urgent.txt from Hotfix
 1 file changed, 1 insertion(+)
 create mode 100644 urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ ls
feature1.txt  feature2.txt  master.txt  urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (hotfix)
$ git checkout main
Switched to branch 'main'

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git branch
  develop
  feature1
  feature2
  hotfix
* main
  release

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ ls
feature1.txt  feature2.txt  master.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git merge hotfix
Updating 9c0f1d5..cd82b93
Fast-forward
 urgent.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ ls
feature1.txt  feature2.txt  master.txt  urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ ls
feature1.txt  feature2.txt  master.txt  urgent.txt

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git pull origin main
From https://github.com/Santhanakumar58/GitworkflowCaseStudy
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
 .github/workflows/Releaseschedule.yml | 40 +++++++++++++++++++++++++++++++++++
 1 file changed, 40 insertions(+)
 create mode 100644 .github/workflows/Releaseschedule.yml

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 561 bytes | 561.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Santhanakumar58/GitWorkflowCaseStudy.git
To https://github.com/Santhanakumar58/GitworkflowCaseStudy.git
   39d4eb6..71d98e7  main -> main

santh@Santhana MINGW64 /c/GitWorkflowCaseStudy (main)
$
