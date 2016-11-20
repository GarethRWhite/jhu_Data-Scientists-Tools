https://www.quora.com/Whats-the-difference-between-git-pulland-git-fetch

git (locally) has a directory (.git) which you commit your files to and this is your 'local repository'.

Merging

Merging is the process of combining code changes from different branches, or from different versions of the same branch (for example when a local branch and remote are out of sync.). If one has developed work in a branch and the work is complete, ready and tested, then it can be merged into the master branch. This is done by:
git checkout master #to switch to the master branch
git pull origin master
git merge your_branch

Once you have resolved any conflicts you will once again git add and git commit those changes to continue the merge



# Branch
https://longair.net/blog/2009/04/16/git-fetch-and-merge/
a name for a particular commit and all the commits that are ancestors of it


git checkout stable   # Change to work on the branch "stable"
git merge new-idea    # Merge in "new-idea"



# Introduction to Git
git config --global user.name "Gareth R. White"
git config --global user.email "GarethRWhite@yahoo.com"
git config --list


https://github.com/GarethRWhite

Create new repo:
https://github.com/new
https://GarethRWhite/jhu_Data-Scientists-Tools
mkdir ~/jhu_Data-Scientists-Tools
cd ~/jhu_Data-Scientists-Tools

git init
git remote add origin https://github.com/GarethRWhite/jhu_Data-Scientists-Tools


# Basic Git Commands

Fork (to current working directory):
git clone https://github.com/GarethRWhite/jhu_Data-Scientists-Tools.git

Review local changes
git status


## Add
Add all new files from cwd
git add .

Push local changes
Update tracking for files that changed names or were deleted
Create new file, add to index
git add -u

Add all new files, and update tracking for files that changed names or were deleted
git add -A


## Commit
Commit to local repository:
git commit

Create new file, add to index, and commit to local repository
git commit -a

Update local repository
git commit -m "useful description of changes"


## Push
Push to remote repository
git push

fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master



##Branches

Create branch
git checkout -b branchname

See what branch you're on
git branch

Switch back to default (master) branch
git checkout master



##Pull

To merge change from your Source branch/repo into (someone elses?) Destination branch/repo
This is a feature of github, not git.
Click "Compare & Pull Request"
Destination branch/repo will be informed of the request, and have the opportunity to review and accept the changes if they want.






#Installing R packages

Obtain R packages from:
CRAN - primary
Bioconductor Project - biological applications
Task Views - lists packages by topic

a <- available.packages()
head(rownames(a), 3) ## Show the names of the first few packages

Install package "slidify" from CRAN:
install.packages("slidify")

Install multiple simultaneously
install.packages(c("slidify", "ggplot2", "devtools"))

###Install from Bioconductor:
http://www.bioconductor.org/install

source("http://bioconductor.org/biocLite.R")
-- Will install a lot of default packages
biocLite()

###Install specific packages
biocLite(c("GenomicFeatures", "AnnotationDbi"))

###Loading R Packages
library(ggplot2)
DO NOT PUT THE PACKAGE NAME IN QUOTES

After loading library, available functions are put in top of search()
search()



# Installing Rtools

## Download Rtools
http://cran.r-project.org/bin/windows/Rtools/

## Install Rtool
If you have cygwin
http://cran.r-project.org/bin/windows/Rtools/Rtools.txt

## Install devtools
find.package("devtools")
install.package("devtools")

## Verify Rtools installation
library(devtools)
find_rtools() # should return TRUE






# Authentication


## Caching your GitHub password in Git
https://help.github.com/articles/caching-your-github-password-in-git/
git config --global credential.helper wincred

## Generating an SSH key
https://help.github.com/articles/generating-an-ssh-key/

### Checking for existing SSH keys
https://help.github.com/articles/checking-for-existing-ssh-keys/
ls -al ~/.ssh

### Adding your SSH key to the ssh-agent
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa

## Adding a new SSH key to your GitHub account
https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
clip < ~/.ssh/id_rsa.pub

https://github.com/settings/keys
Add new SSH key
Title: Git Bash on SHA-WKS-AB688




# Pages
https://pages.github.com/

##Create a new repository
https://github.com/new
Repository name: garethrwhite.github.io

cd ~
git clone https://github.com/garethrwhite/garethrwhite.github.io
cd garethrwhite.github.io
echo "Hello World" > index.html
git add --all
git commit -m "Initial commit"
git push -u origin master

https://garethrwhite.github.io/
