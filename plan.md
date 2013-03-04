Intro
History of version control
My First project
	mkdir my-git-project
	cd my-git-project
	git init
	touch README.md
	git commit -m 'First commit'

Files status and Lifecycle
	git status
	vi README.md 	# add project title 'my-git-project' in markdown syntax
	git status
	git add
	git status
	git commit -m 'Add title to readme'
	git status
	git log

	touch useless-file.txt
	vi README.md	# add Overview subtitle and description
	git status
	git add README.md
	git commit -m 'Add overview section to doc'
	git status
	
	git add useless-file.txt
	git status
	git reset --cached useless-file.txt

Lifecycle slide
Clone GitHub Project
	Go to https://github.com/jlalande/webapp-demo
	git clone https://github.com/jlalande/webapp-demo.git
	
	ls -l
	mvn jetty:run
	http://localhost:8080/hello
	
	git remote
	git remote show origin
	
Add feature to GitHub Project
	git branch feature/root-resource
	git checkout feature/root-resource	# git checkout -b feature/root-resource
	
	copy HelloWorldResource.java to RootResource.java
	modify @Path
	modify method name and returned value. Value should be HTML page (via copy/paste)
	
	git status
	git commit -a -m 'Add a root resource'
	git status
	
	git push origin master

Merge feature branch into master branch

	git checkout master
	git merge feature/root-resource
	
Pull/Fetch
	git checkout master
	modify README.md via GitHub
	
	git fetch
	git merge
	
	modify README.md again
	
	git pull
	
Stashing
	modify README.md, add useless line
	
	git stash
	
	modify README.md with another title
	
	git stash
	
	git stash show
	
	modify README.md somewhere else
	git stash apply
	
	git stash drop STASH

