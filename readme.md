#Topics to cover#
Single developer workflow for easy getting started.

##GIT (really simple explained)##
* git is a local version control software which can also push/pull changes to a remote repository
* commit is equivalent to a checkpoint 
* branch is a separate line of code.

##Git basic workflow##

* single branch
* branch per feature
* branch per release

#Basic Commands#

* git init
* Only first time configuration 
*  * git config --global user.name "John Doe"
*  * git config --global user.email johndoe@example.com
* git status
* git add .
* git commit -m "My custom message"
* git log

##Reset commits
* git reset --soft HEAD~1 (undo last commit) 

##Tags
They annotate (tag) specific points in history such a releases or any other important checkpoint. Its useful when specifying releases. Also github creates a link directly to releases as zip so other users can download the repo as a zip file.

* git tag v1.0.0 (simple tag)
* git tag -a v1.0.0 -m "release v1.0.0" (message must be descritive as it will show up in github pages"
* git tag (shows existing tags)
* git tag v1.0.0 (will show the commit of the current tag)
* git tag -D v1.0.0 (will remove the tag)
* git push origin :refs/tags/v1.0.0 (will remove the tag remotely)

Tags are not pushed by default you have to do it manually

* git push origin --tags (pushes all tags)
* git push origin v1.0.0 (pushes only the specified tag)
 
##branching##
* git branch
* git branch myBranchName
* git checkout myBranchName
* git merge nameOfBranch

##Remote repositories##
* git remote add origin url
* git push -u origin branchName
* git remote -v (shows current remote repositories) 
* git remote set-url origin https://github.com/username/repo-name.git (the url is the new repo)

##update .gitignore
* git rm -r --cached .
* git add .
* git commit -m "gitignore updated"

