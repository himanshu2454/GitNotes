# git  
> Git is "distributed Version Control System"
**Types of VCS** - 
1. **Central VCS**    
+ Whole Repo. is situated at one place.
+ User commit to the central location but don't have whole code base.
+ In case of corruption, whole repo is lost/Corrupted.
2. **Distributes VCS**  
- Repo is distrubuted across the users.
- Users commit to central location but at same also has the latest copy of the code base.
- In case of corruption at one site others can still use it.
# Initial Setup
 1. **Download from**  
- https://git-scm.com/downloads
 2. **check the version**
```
 git version ( gives the current version of git)
```
3. **Set Config Values**
```
git config --global user.name "<username>"  
git config --global user.email "<email>"  
git config --list ( To check config values)
```
4. **Help**  
```  
git help <verb>  
git <verb> --help  
E.g -  
git help config  
git config --help
```
# Getting Started
## 1. **Initialize Repo. from existing Code base.**
### Intialize repo
```
git init  
Initialize repo in the current working directory.
Creates a ".git" dir.
```
### .gitignore  
- Contains all the file or wildcards, which need not be tracked.
- usually the file that has local or personal settings like .vs 
```
E.g  
-- .gitignore --  
.proj  
random.cs  
*.py
```
### Areas in git
```
Working Dir ---> Staging Area ---> .git Dir(Repository)  
   |<--------- checkout the Project ----------(.)  
(.)---staging fixes---->|  
                        (.)------commit-------->|
```
### Stages of file
1. **Get status**    
```
git status
Gives details of tracked,untracked, stagged,unstaged files.
```
2. **Stage a file**
```
git add -A
git add <filename>
```
3. **Unstage file/s**  
```
git reset 
git restrore --staged filename
```
4. **Commit Staged changes**
```
git commit -m "msg"
```
5. **Get Commit logs**
```
git log
```
## 2. Working on a remote repository*
### Clone a repo.
```
git clone <url> <where to clone>
E.g
git clone https://github.com/himanshu2454/CSharpFundamentalsNotes.git .
```
### Viewing info. about remote repo.
1. **Location of remote repo**
```
git remote -v
```
2. **List all the branches local as well as remote**  
```
git branch -a
```
3. **Get diff**
```
git diff
```
### Pull
##### Usage: To fetch updates from the remote repo. if any.
```
git pull origin master
origin -- Name of remote repo.
master -- Remote branch.
```
### Push
##### Usage: To push commited changes.
```
git push origin master
```

# Working with branches
1. **Create a branch**
```
git branch <BranchName>
#To point to specific branch.
git checkout <BranchName>
```
2. **List of branches**
```
git branch
Lists all the branches 
```
3. **Commit branch to remote repo**
```
git push -u origin <BranchName>
-u -- to let the vcs know both remote and local branch are same.
```
4. **Merge with master**
```
git checkout master
git pull origin master
git merge --merged
:- Lists all the merged branchs so far
git merge <BrachName>
git push origin master
```
5. **Delete used Branch**
```
git branch -d <BranchName>
:- This is delets locally
git push origin --delete <BranchName>
:- Deletes branch from remote repo.
```
