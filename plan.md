### Intro

### History of version control

### My First project

Show *Let's create my first project!* slide.

Create a first local project from an empty directory.

```bash
mkdir my-git-project
cd my-git-project
git init
touch README.md
git add .
git commit -m 'First commit'
```

### File status Lifecycle

- Show project status at different phases.
- Modify existing file 
- Add modified file to staging area
- Commit file

```bash
git status
vi README.md 	# add project title 'my-git-project' in markdown syntax
git status
git add README.md
git status
git commit -m 'Update README.md with title'
git status
git log
```

Explain difference between new files and new files added to staging area.

```bash
touch useless.txt
vi README.md	# add Overview subtitle and description
git status
git add README.md
git commit -m 'Update README.md with an overview and description'
git status

# Add and remove useless file
git add useless.txt
git status
git reset HEAD useless.txt
```

### Lifecycle slide

Show *Lifecycle* slide.

### Clone GitHub Project

Show *Let's clone a project!* slide.

Go to https://github.com/jlalande/webapp-demo and copy clone link.

```bash
# Clone project from GitHub
git clone https://github.com/jlalande/webapp-demo.git
cd webapp-demo

# Run the embedded Jetty
mvn jetty:run	# Point your browser to http://localhost:8080/hello

# Show remote repository
git remote
git remote show origin
```	

### Add feature to GitHub Project

```bash
git branch feature/root-resource
git checkout feature/root-resource	# git checkout -b feature/root-resource

# copy HelloWorldResource.java to RootResource.java
# modify @Path to "/"
# modify method name to getRoot
# replace @Provide with "text/html"
# replace return value with HTML page (via copy/paste)
	
git status
git add .

git checkout master
git status	# just added file is available even when switching branch

git checkout feature/root-resource
git commit -m 'Add root resource'
git status

git checkout master
ls src/main/java/com/jlalande	# Resource commited in feature branch is not available in master

git checkout feature/root-resource
ls src/main/java/com/jlalande

git push origin feature/root-resource
```

### Merge feature branch into master branch

```bash
git checkout master
git merge feature/root-resource

ls src/main/java/com/jlalande	# Root resource is now available
git branch

git push origin master
```

### Pull/Fetch

```bash
git checkout master
# modify README.md via GitHub

git fetch
git merge

# modify README.md again

git pull
```

### Workflow

Show *Workflow* slide.

### Stashing

```bash
# modify README.md, add useless line

git stash

# modify README.md with another title
	
git stash
git stash show

# modify README.md somewhere else
git stash apply
git stash drop STASH
```

### Branching model

Show *Branching Model* slide and the rest of the presentation.
