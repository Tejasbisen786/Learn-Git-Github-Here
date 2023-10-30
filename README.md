# Git and Github Notes
   - github - where all folder and file are stored
    - github  provide the services<br>
   -git - giving control over the files and folder by introducing some command
   git- version control system <br>

   -- all the changes can be modifed and track the whole histroy of the project
   <br>
  
   download CLI for better undestaading

# Basic Linux Command

mkdir - making a folder<br>
ls- listing a whole file present over a file<br>
cd - Change Directory<br>
ls-a : listing hidden file<br>
ls .< file folder >: showing the content of folder<br>
touch- to create a file name<br>
cat: to see the conntent inside the file <br>
rm -rf : recursive delete the files<br>


# Git command
git init : initilizing the the git <br>
git status- tracking the file whether chaged made happened or not <br>
git add : adding file into staging area from local working area <br>
git add . : putting all files into staging area<br>
git commit -m " < message >" : commiting all changes from the files  <br>
git restore --staged < file_name >: to unstaged the file  <br>
git log : to show all commited history  <br>
git reset < commit hash > : reset the commit ( redo the previous commit ) <br>
git stash: holding all commit  and whenverneed let's brings all back into the staging area  <br>
git stash pop : bringing holding all commit from backstaged to staging area <br>
git stash clear: removing all holding commited in back-staged <br>
git remote add < Name of the url > < repo url>: connecting repo with your local folders<br>
git remote -v: listing all the remote url <br>
git push < url name > < branch name> : pushing file into github remote file <br>
git branch < branch name>: making new feature branch  <br>
git checkout < branch name> : to get into the branch means header point current branch  <br>
git merge <> : merging new feature into default  <br>
from where you're forked url called upsteam: 
git add remote upstream < repo url >:  
* balancing upstream and fork changed constant *
ex: <br>
git cheackout master: <br>
git fetch -all --prune  <br>
git reset --hard upstream/main <br>
git push origin main  <br>
<br>
or 
git pull upstream main 
git push origin main




<br>

git clone < repo url> : cloning file from remote server to your local machine
<br>
fork: BY Fork repository this repo will enable into yor account and you're able to work with this.


<br>


 <h5> Note </h5>
** Never commit on main branch ( by default),
instead for any new feature make a new branch and after finalized features merge final feature with the main , so that if new user want to clone project it will going to direcly clone the main **
<br>
** Mostly Project deployed using main brach it means the main branch in on the production" 
<br>

<h2> Github Most Common issue</h2>

-  Steps to change github branch default from master to main  
 Step 1 
- create main branch locally, taking the history from master
git branch -m master main

 - Step 2 
 push the new local main branch to the remote repo (GitHub) 
git push -u origin main

- Step 3
 switch the current HEAD to the main branch
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main

-  Step 4
 -change the default branch on GitHub to main
 - https://docs.github.com/en/github/administering-a-repository/setting-the-default-branch

- Step 5
-  delete the master branch on the remote
git push origin --delete master

# While pushing fetch refs couldn't find issue [Fetch issue]
- try this code : <br>
- git fetch origin main:tmp
- git rebase tmp
- git push origin HEAD:main
- git branch -D tmp
- git push -u origin main

<h2> Quick Git Setup Command </h2>

- echo "# task2" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin git@github.com:tusharbisen/task2.git
- git push -u origin main