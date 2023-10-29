# Git and Github Notes
   - github - where all folder and file are stored
    - github  provide the services
   -git - giving control over the files and folder by introducing some command
   git- version control system 

   -- all the changes can be modifed and track the whole histroy of the project
  
   download CLI for better undestaading
   - 

# Basic Linux Command

mkdir - making a folder
ls- listing a whole file present over a file
cd - Change Directory
ls-a : listing hidden file
ls .< file folder >: showing the content of folder
touch- to create a file name
cat: to see the conntent inside the file 
rm -rf : recursive delete the files


# Git command
git init : initilizing the the git
git status- tracking the file whether chaged made happened or not
git add : adding file into staging area from local working area
git add . : putting all files into staging area
git commit -m " < message >" : commiting all changes from the files 
git restore --staged < file_name >: to unstaged the file 
git log : to show all commited history 
git reset < commit hash > : reset the commit ( redo the previous commit )
git stash: holding all commit  and whenverneed let's brings all back into the staging area
git stash pop : bringing holding all commit from backstaged to staging area
git stash clear: removing all holding commited in back-staged
git remote add < Name of the url > < repo url>: connecting repo with your local folders
git remote -v: listing all the remote url
git push < url name > < branch name> : pushing file into github remote file
git branch < branch name>: making new feature branch 
git checkout < branch name> : to get into the branch means header point current branch 
git merge <> : merging new feature into default file
from where you're forked url called upsteam: 
git add remote upstream < repo url >: 
* balancing upstream and fork changed constant *
ex:
git cheackout master:
git fetch -all --prune 
git reset --hard upstream/main
git push origin main 

or 
git pull upstream main 
git push origin main






git clone < repo url> : cloning file from remote server to your local machine

fork: BY Fork repository this repo will enable into yor account and you're able to work with this.










** Never commit on main branch ( by default),
instead for any new feature make a new branch and after finalized features merge final feature with the main , so that if new user want to clone project it will going to direcly clone the main **

** Mostly Project deployed using main brach it means the main branch in on the production" 