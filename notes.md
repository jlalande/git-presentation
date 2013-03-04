introduction
------------

example of git init

`touch README.md` (useful in Github/Gitlab)

`git commit -m 'first commit'`

`git status`

`git diff`


cloning
-------

cloning from github sample project

	this project must have a pom.xml file with scm already configured for showing a full release with tagging

SSH vs HTTPS

local vs remote

multiple remote

centralized remote repository vs fetching changes from co-workers


branching
---------

`git branch BRANCH`

`git checkout BRANCH`

`git checkout -b NEW_BRANCH`

everything is a branch

git development diagram with master and devel branches => should it be placed toward the end?


staging area
------------

staging area: `git add`, `git add FILE`, `git add .`

`git commit`

`git commit -v`

`git commit -a`

`git commit --amend`


stash
-----
`git stash`

`git stash pop`

`git stash apply`

`git stash drop`


unstaging & revert
------------------
`git reset HEAD FILE`

`git checkout HEAD FILE`


merging
-------
in branch, `git commit -m 'commit before merge'`

`git checkout master`

`git merge feature/branch`

Automatic merge
fix conflicts

`git add FILE or git add .`

`git commit -m 'Merge to master'`

`git mergetool`


remote
------
`git remote -v`

`git remote add [shortname] [url]`

`git push`

`git push origin master`

`git push [remote-name] [branch-name]`

`git fetch`

`git merge`

`git pull`

`git remote rename old-branch new-branch`

`git remote rm unused-branch`


rebasing
--------
Where should it be?

useful to clean history

Do not rebase commits that you have pushed to a public repository.


references
----------

Official Git Web site: http://git-scm.com/

Markdown syntax: http://daringfireball.net/projects/markdown

GitHub: https://github.com/

GitLab: http://gitlab.org/

TortoiseGit: https://code.google.com/p/tortoisegit/


