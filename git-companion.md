### Create a github project mirrored to your local computer.

go to your github account
new repository
choose a repository-name
set public
add a readme file
add a .gitignore if the case
choose a license

don't create the folder! it will be created with the repo name on github
git clone https://github.com/gustcomer/reponame.git


VS Code can do this process of creating the github repo for you

You can't first create a local repository and then create the github counterpart

You can do all in the command line without entering the github.com website if
you gave github cli installed in your local machine

## Clone a other person's repository as a template

- just go to the github repository page, and select "use this repository as a
template"

### Commit changes to the local git and then push to github

create/change some files
> git status | check if everything is ok
> git add -A | add all files that were changed
ou > git add .
> git commit -m "git-companion: initial"
[once] > git remote add origin https://github.com/gustcomer/big-tech-companions
  actually it's not necessary because the clone already sets origin
[once] > git push -u origin main
[after] > git push

### .gitignore

/ at the begining - the pattern is relative to the .gitignore directory
node_modules/ - node_modules directory @ root of the git project (absolute)
/node_modules/ - node_modules directory @ .gitignore folder (relative)
node_modules - node_modules directory or node_modules file

A leading "**" followed by a slash means match in all directories. For example,
"**/foo" matches file or directory "foo" anywhere, the same as pattern "foo".

An asterisk "*" matches anything except a slash. Including many characters
except /.

*.excalidraw - all files ending with .excalidraw in any folder or subfolder.

The character "?" matches any one character except "/".

### stash in vscode

just click Uncommitted Changes with right button and choose a name
when you stash, the last commit rolls back

#### How to update the windows local version of git

> git update-git-for-windows