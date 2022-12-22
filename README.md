# Payment-gateway-intergration-
Website for payment gateway Integration 
Customer. A customer presses a “Purchase” button and fills in the necessary fields to pass the transaction data. The data is encrypted and sent to the merchant’s web server via an SSL connection.
Merchant and payment gateway. After the transaction data is received, a merchant passes it to the payment gateway via another encrypted SSL channel. If any of data is stored by a payment gateway, it is settled in a specific type of secured storage. Usually, gateways don’t store actual credit card numbers, but rather save tokens.
Payment processor. The information goes to payment processors. These are the companies that provide payment processing services as third-party players. Payment processors are connected both with a merchant’s account and a payment gateway, transferring data back and forth. At that stage, a payment processor is passing the transaction to a card network (Visa, Mastercard, American Express, etc.).
Visa/Mastercard/American Express/Discover. The role of a card network is to verify the transaction data and pass it to the issuer bank (the bank that produced the cardholder’s credit/debit card).
DevOps Handouts
1.Working with GIT, checking status and committing in local machine.
->4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>abc.txt
RIT

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls abc.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
No commits yet
Untracked files:
(use "git add <file>..." to include in what will be committed) abc.txt
nothing added to commit but untracked files present (use "git add" to track)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git add abc.txt
warning: in the working copy of 'abc.txt', LF will be replaced by CRLF the next time Git touches it
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git commit -m "created for a practice purpose"
[master (root-commit) 4d570c3] created for a practice purpose
1 file changed, 1 insertion(+)
create mode 100644 abc.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
nothing to commit, working tree clean
2.Adding multiple files in local machine.
->
4mca@MCALAB-009 (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>a.txt
HII

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>b.txt
Hello

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
No commits yet
Untracked files:
(use "git add <file>..." to include in what will be committed) a.txt
b.txt
nothing added to commit but untracked files present (use "git add" to track)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git add -A
warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git commit -a -m"added"
[master (root-commit) edbdd8b] added 2 files changed, 2 insertions(+) create mode 100644 a.txt
create mode 100644 b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt
3.Creating a new branch add texts in that and merge that files with master.
->4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>a.txt
hii

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>b.txt
hello

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
No commits yet
Untracked files:
(use "git add <file>..." to include in what will be committed) a.txt
b.txt

nothing added to commit but untracked files present (use "git add" to track)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git add -A
warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git commit -a -m "added"
[master (root-commit) ee44bf0] added 2 files changed, 2 insertions(+) create mode 100644 a.txt
create mode 100644 b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
nothing to commit, working tree clean
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt
4mca@MCALAB-009 (master)
$ git branch firstbranch
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git checkout firstbranch
Switched to branch 'firstbranch'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ ls
a.txt b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ cat>>c.txt
namaste

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ ls
a.txt b.txt c.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ git add c.txt
warning: in the working copy of 'c.txt', LF will be replaced by CRLF the next time Git touches it

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ git commit -m "added c.txt"
[firstbranch 9a1b11a] added c.txt 1 file changed, 1 insertion(+)
create mode 100644 c.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ ls
a.txt b.txt c.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)

$ git checkout master
Switched to branch 'master'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git checkout firstbranch
Switched to branch 'firstbranch'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ ls
a.txt b.txt c.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (firstbranch)
$ git checkout master
Switched to branch 'master'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git merge firstbranch
Updating ee44bf0..9a1b11a Fast-forward
c.txt | 1 +
1 file changed, 1 insertion(+)
create mode 100644 c.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt c.txt
4.Renaming a branch, pull the data from GitHub make changes and then push to GitHub.
->
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git branch -m main
Create new repository ->name->public->add a read readMe file
Modify in github if needed(adding content)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git remote add origin "https://github.com/VasanthaNagaraj/VN.git"
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git pull origin main remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done. remote: Compressing objects: 100% (3/3), done.
remote: Total 7 (delta 0), reused 0 (delta 0), pack-reused 0 Unpacking objects: 100% (7/7), 1.74 KiB | 98.00 KiB/s, d
one.
From https://github.com/VasanthaNagaraj/VN
* branch main -> FETCH_HEAD
* [new branch] main -> origin/main
Make changes in local machine

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git add .
4mca@MCALAB-009 (main)
$ git commit -m"changed"
[main 18877d7] changed
1 file changed, 1 insertion(+)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git status
On branch main
nothing to commit, working tree clean
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 251 bytes | 251.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 To https://github.com/VasanthaNagaraj/VN.git b5e5f9a..18877d
7 main -> main

......................................................................
5.When you want to merge with master then checkout to master(MERGE CONFLICT).
->
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (firstbranch)
$ git init
Initialized empty Git repository in C:/Users/91733/Desktop/Vasantha/.git/
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat>>a.txt
Hello

91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat>>b.txt
Hii

91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git add . warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it warning:
in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git commit -m "created two text files"
[master (root-commit) 7805c87] created two text files
2 files changed, 2 insertions(+) create mode 100644 a.txt
create mode 100644 b.txt
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat a.txt
Hello
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)

$ git branch f1
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git branch f2
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git checkout f1
Switched to branch 'f1'
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f1)
$ cat a.txt
Hello
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f1)
$ git add . warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f1)
$ git commit -m"changed a.txt in f1"
[f1 892ae42] changed a.txt in f1
1 file changed, 1 insertion(+)
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f1)
$ cat a.txt
Hello
Gud Night
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f1)
$ git checkout master
Switched to branch 'master'
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat a.txt
Hello
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git merge f1
Updating 7805c87..892ae42 Fast-forward
a.txt | 1 +
1 file changed, 1 insertion(+)
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat a.txt
Hello
Gud Night
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git checkout f2
Switched to branch 'f2'
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f2)
$ cat a.txt
Hello
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f2)
$ git add .
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f2)

$ git commit -m"changed a.txt in f2"
[f2 5557927] changed a.txt in f2
1 file changed, 1 insertion(+)
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f2)
$ cat a.txt
Hello
Bye
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (f2)
$ git checkout master
Switched to branch 'master'
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat a.txt
Hello
Gud Night
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git merge f2
Auto-merging a.txt
CONFLICT (content): Merge conflict in a.txt
Automatic merge failed; fix conflicts and then commit the result.
RESOLVING BY MERGE TOOL
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master|MERGING)
$ git mergetool
This message is displayed because 'merge.tool' is not configured.
See 'git mergetool --tool-help' or 'git help config' for more details.
'git mergetool' will now attempt to use one of the following tools:
opendiff kdiff3 tkdiff xxdiff meld tortoisemerge gvimdiff diffuse diffmerge ecmerge p4merge araxis bc codecompar
e smerge emerge vimdiff nvimdiff Merging:
a.txt
Normal merge conflict for 'a.txt':
{local}: modified file
{remote}: modified file
Hit return to start merge resolution tool (vimdiff):
4 files to edit
ENTER

Remove <<<head using i then shift + then :wq enter do this process three times
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master|MERGING)
$ git status
On branch master
All conflicts fixed but you are still merging. (use "git commit" to conclude merge) Changes to be committed:
modified: a.txt
Untracked files:
(use "git add <file>..." to include in what will be committed) a.txt.orig
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master|MERGING)
$ git add .

91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master|MERGING)
$ git commit -m "Resolved merge conflict"
[master dc0b00b] Resolved merge conflict
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ git merge f2 Already up to date.
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/Vasantha (master)
$ cat a.txt
Hello
Gud Night
Bye
.........................................................................
6.How to revert back to the previous version.
->
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ git init
Reinitialized existing Git repository in C:/Users/91733/Desktop/VN/.git/
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ cat >>a.txt
Hii

91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ git add . warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ git commit -m"added"
[master (root-commit) 3b6acb0] added 1 file changed, 3 insertions(+)
create mode 100644 a.txt
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ cat a.txt
Hii
Vasantha

91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ git log
commit 3b6acb087c1b6e234003ddfb8f7de59cc7ac8398 (HEAD -> master)
Author: Vasantha Nagaraj <vasanthajalaja4@gmail.com>
Date: Tue Dec 13 22:51:10 2022 +0530
added
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ git checkout 3b6acb08 a.txt
Updated 0 paths from 977fc1d
91733@DESKTOP-VF5T9OD MINGW64 ~/Desktop/VN (master)
$ cat a.txt
Hii
Vasantha
........................................................................

7.Create a local branch (push the branch to GitHub) add on some file to it.
->
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/ 4mca@MCALAB-009 MINGW64 ~/Deskt
op/DevOps (master)
$ git remote add origin "https://github.com/VasanthaNagaraj/VN.git"
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git pull origin main remote: Enumerating objects: 13, done. remote: Counting objects: 100% (13/13), done. remote
: Compressing objects: 100% (5/5), done. remote: Total 13 (delta 0), reused 3 (delta 0), pack-reused 0 Unpacking ob
jects: 100% (13/13), 2.57 KiB | 119.00 KiB/s, done.
From https://github.com/VasanthaNagaraj/VN
* branch main -> FETCH_HEAD
* [new branch] main -> origin/main
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git branch feature
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git checkout feature
Switched to branch 'feature'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ cat>>vn.txt
GOOD MORNING

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ git add . warning: in the working copy of 'vn.txt', LF will be replaced by CRLF the next time Git touches it
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ git commit -m"created vn.txt in feature branch"
[feature 10ff9cf] created vn.txt in feature branch
1 file changed, 1 insertion(+)
create mode 100644 vn.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ ls
README.md vn.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ git checkout master
Switched to branch 'master'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
README.md
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git checkout feature
Switched to branch 'feature'
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (feature)
$ git push origin feature

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 287 bytes | 287.00 KiB/s, done. Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 rem
ote: remote: Create a pull request for 'feature' on GitHub by visiting:
remote: https://github.com/VasanthaNagaraj/VN/pull/new/feature remote:
To https://github.com/VasanthaNagaraj/VN.git
* [new branch] feature -> feature
In GitHub->compare and pull->merge pull request->confirm merge.
........................................................................
8.Cloning.
Cloning a repository gives you a copy of that repository and configures the original repository as a remote. Copying
a repository just gives you a copy of that repository.

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>a.txt
hii

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ cat>>b.txt
hello

4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git add . warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git commit -a -m "added two text files"
[master (root-commit) 3cf09c8] added two text files
2 files changed, 2 insertions(+) create mode 100644 a.txt
create mode 100644 b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git status
On branch master
nothing to commit, working tree clean
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
a.txt b.txt
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git branch vasantha
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master) $ git clone "https://github.com/VasanthaNagaraj/M
CA.git" Cloning into 'MCA'...

remote: Enumerating objects: 10, done. remote: Counting objects: 100% (10/10), done. remote: Compressing objects
: 100% (4/4), done. remote: Total 10 (delta 0), reused 3 (delta 0), pack-reused 0 Receiving objects: 100% (10/10), do
ne.
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ ls
MCA/ a.txt b.txt
.....................................................................
9.Fetch.
->
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (main)
$ git init
Initialized empty Git repository in C:/Users/4mca/Desktop/DevOps/.git/
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git fetch origin main fatal: 'origin' does not appear to be a git repository fatal: Could not read from remote repositor
y.
Please make sure you have the correct access rights and the repository exists.
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git remote add origin "https://github.com/VasanthaNagaraj/VASANTHA.git"
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git fetch origin main remote: Enumerating objects: 13, done. remote: Counting objects: 100% (13/13), done. remot
e: Compressing objects: 100% (6/6), done. remote: Total 13 (delta 0), reused 6 (delta 0), pack-reused 0 Unpacking o
bjects: 100% (13/13), 2.26 KiB | 96.00 KiB/s, done.
From https://github.com/VasanthaNagaraj/VASANTHA
* branch main -> FETCH_HEAD
* [new branch] main -> origin/main
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git merge origin/main
Updating b4a2cc7..090c491
Fast-forward
README.md | 1 +
1 file changed, 1 insertion(+)
4mca@MCALAB-009 MINGW64 ~/Desktop/DevOps (master)
$ git log
commit 090c4916db182f6455b59b353290ce1fa5561d45 (HEAD -> master, origin/main)
Author: VasanthaNagaraj <112241640+VasanthaNagaraj@users.noreply.github.com> Date: Wed Dec 14 15:56:37
2022 +0530
Update README.md
commit b4a2cc79b188569052efde996ddf2358a14bd1c0
Merge: 8a45f4a a47ba51
Author: VasanthaNagaraj <112241640+VasanthaNagaraj@users.noreply.github.com> Date: Tue Dec 13 15:06:58
2022 +0530
Merge pull request #1 from VasanthaNagaraj/feature
created aa.txt in feature branch

commit a47ba51c520d53aedd1cccdee53edc7a4da5954e
Author: Bob <bob@gmail.com>
Date: Tue Dec 13 15:00:43 2022 +0530
created aa.txt in feature branch
commit 8a45f4a3f8bd039170be0f95dccf5bf8a539e4e7
Author: Bob <bob@gmail.com>
Date: Fri Dec 9 09:54:10 2022 +0530
changed in local
commit bea414e3f9bd2bf3544d614c39503fec5894672f
Author: VasanthaNagaraj <112241640+VasanthaNagaraj@users.noreply.github.com> Date: Fri Dec 9 09:37:50 20
22 +0530
CHANGES
commit 35f6aeba8931350ae16be8e75dfc14ecda633bde
Author: VasanthaNagaraj <112241640+VasanthaNagaraj@users.noreply.github.com>
Date: Fri Dec 9 09:37:29 2022 +0530
Initial commit

.........................................................................
compare and pull reqest
10.
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1
$ git init
Initialized empty Git repository in B:/office1/.git/
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git remote add origin https://github.com/swapnil05sahu/office.git
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git pull origin master
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 595 bytes | 66.00 KiB/s, done.
From https://github.com/swapnil05sahu/office
* branch master -> FETCH_HEAD
* [new branch] master -> origin/master
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git branch office1
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git branch offcie2
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)

$ git checkout office1
Switched to branch 'office1'
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (office1)
$ git add .
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (office1)
$ git commit -m "added"
[office1 69d50ba] added
2 files changed, 0 insertions(+), 0 deletions(-)
create mode 100644 a.txt.txt
create mode 100644 b.txt.txt
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (office1)
$ git status
On branch office1
nothing to commit, working tree clean
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (office1)
$ ls
README.md a.txt.txt b.txt.txt
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (office1)
$ git checkout master
Switched to branch 'master'
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git push origin office1
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 275 bytes | 275.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'office1' on GitHub by visiting:
remote: https://github.com/swapnil05sahu/office/pull/new/office1
remote:
To https://github.com/swapnil05sahu/office.git
* [new branch] office1 -> office1
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git checkout office2
error: pathspec 'office2' did not match any file(s) known to git
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git checkout offcie2
Switched to branch 'offcie2'
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (offcie2)
$ git add .
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (offcie2)
$ git commit -m "added"
[offcie2 0ccb6b9] added

1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 c.txt
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (offcie2)
$ ls
README.md c.txt
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (offcie2)
$ git checkout master
Switched to branch 'master'
swapn@LAPTOP-05TD7ESK MINGW64 /b/office1 (master)
$ git push origin offcie2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 269 bytes | 269.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'offcie2' on GitHub by visiting:
remote: https://github.com/swapnil05sahu/office/pull/new/offcie2
remote:
To https://github.com/swapnil05sahu/office.git
* [new branch] offcie2 -> offcie2
Issuer bank. The issuer bank also accepts or denies the authorization request. In response, a bank sends a code back to the payment processor, which contains the transaction status or error details.
Payment gateway. Transaction status is returned to the payment gateway, then passed to the website.
Customer and issuing bank. A customer receives a message with the transaction status (accepted or denied) via a payment system interface.
Issuer bank. Within a couple of days (generally the next day), the funds are transferred to the merchant’s account. The transaction is performed by the issuing bank to the acquiring bank.
