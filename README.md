# git-testing2
PS C:\Users\aslam\Desktop\git-testing2> git clone https://github.com/Aslam-Moinuddin/git-testing2.git .
Cloning into '.'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
PS C:\Users\aslam\Desktop\git-testing2> git remote -v  
origin  https://github.com/Aslam-Moinuddin/git-testing2.git (fetch)
origin  https://github.com/Aslam-Moinuddin/git-testing2.git (push)
PS C:\Users\aslam\Desktop\git-testing2> git remote add upstream https://github.com/Aslam-moin/git-testing2.git
PS C:\Users\aslam\Desktop\git-testing2> git remote -v
origin  https://github.com/Aslam-Moinuddin/git-testing2.git (fetch)
origin  https://github.com/Aslam-Moinuddin/git-testing2.git (push)
upstream        https://github.com/Aslam-moin/git-testing2.git (fetch)
upstream        https://github.com/Aslam-moin/git-testing2.git (push)
PS C:\Users\aslam\Desktop\git-testing2> git branch
* main
PS C:\Users\aslam\Desktop\git-testing2> git checkout develop
branch 'develop' set up to track 'origin/develop'.
Switched to a new branch 'develop'
PS C:\Users\aslam\Desktop\git-testing2> git branch
* develop
  main
PS C:\Users\aslam\Desktop\git-testing2> git fetch upstream 
From https://github.com/Aslam-moin/git-testing2
 * [new branch]      develop    -> upstream/develop
 * [new branch]      main       -> upstream/main
PS C:\Users\aslam\Desktop\git-testing2> git merge upstream/develop
Already up to date.
PS C:\Users\aslam\Desktop\git-testing2> git push origin develop
Everything up-to-date
PS C:\Users\aslam\Desktop\git-testing2> git checkout -b feature/index
Switched to a new branch 'feature/index'
PS C:\Users\aslam\Desktop\git-testing2> git add .
PS C:\Users\aslam\Desktop\git-testing2> git commint -m "add index.html"
git: 'commint' is not a git command. See 'git --help'.

The most similar command is
        commit
PS C:\Users\aslam\Desktop\git-testing2> git commit -m "add index.html" 
[feature/index 6938c3d] add index.html
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing2> git push push -u origin feature/index
fatal: 'push' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\aslam\Desktop\git-testing2> git push -u origin feature/index     
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 426 bytes | 426.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'feature/index' on GitHub by visiting:
remote:      https://github.com/Aslam-Moinuddin/git-testing2/pull/new/feature/index
remote:
To https://github.com/Aslam-Moinuddin/git-testing2.git
 * [new branch]      feature/index -> feature/index
branch 'feature/index' set up to track 'origin/feature/index'.
PS C:\Users\aslam\Desktop\git-testing2> git push origin feature/index
Everything up-to-date
PS C:\Users\aslam\Desktop\git-testing2> git branch
  develop
* feature/index
  main
PS C:\Users\aslam\Desktop\git-testing2> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\aslam\Desktop\git-testing2> git checkout develop
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.
PS C:\Users\aslam\Desktop\git-testing2> git pull upstream/develop
fatal: 'upstream/develop' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\aslam\Desktop\git-testing2> git pull upstream develop
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 899 bytes | 29.00 KiB/s, done.
From https://github.com/Aslam-moin/git-testing2
 * branch            develop    -> FETCH_HEAD
   7e9a533..c6d2699  develop    -> upstream/develop
Updating 7e9a533..c6d2699
Fast-forward
 index.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing2> git push origin develop
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing2.git
   7e9a533..c6d2699  develop -> develop
PS C:\Users\aslam\Desktop\git-testing2> git log --oneline
c6d2699 (HEAD -> develop, upstream/develop, origin/develop) Merge pull request #1 from Aslam-Moinuddin/feature/index
6938c3d (origin/feature/index, feature/index) add index.html
7e9a533 (upstream/main, origin/main, origin/HEAD, main) Initial commit
PS C:\Users\aslam\Desktop\git-testing2> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\aslam\Desktop\git-testing2> git pull upstream main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 887 bytes | 73.00 KiB/s, done.
From https://github.com/Aslam-moin/git-testing2
 * branch            main       -> FETCH_HEAD
   7e9a533..a5850eb  main       -> upstream/main
Updating 7e9a533..a5850eb
Fast-forward
 index.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing2> git push origin main   
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing2.git
   7e9a533..a5850eb  main -> main
PS C:\Users\aslam\Desktop\git-testing2> git log --oneline
a5850eb (HEAD -> main, upstream/main, origin/main, origin/HEAD) Merge pull request #2 from Aslam-moin/develop
c6d2699 (upstream/develop, origin/develop, develop) Merge pull request #1 from Aslam-Moinuddin/feature/index
6938c3d (origin/feature/index, feature/index) add index.html
7e9a533 Initial commit
PS C:\Users\aslam\Desktop\git-testing2> git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\aslam\Desktop\git-testing2> 