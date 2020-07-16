



## GIT 

## Version Control  

### Prerequisites

The prerequisites are given below
```
*Github, gitlab account 
*Git Bash
```
### Installing
Install Git Bash - [Click Here](https://git-scm.com/downloads) 
### GIT commands

Git is the industry-standard version control system for web developers
Use Git commands to help keep track of changes made to a project:

* ``git init`` creates a new Git repository
* ``git status`` inspects the contents of the working directory and staging area
* ``git add`` adds files from the working directory to the staging area
* ``git diff`` shows the difference between the working directory and the staging area
* ``git commit`` permanently stores file changes from the staging area in the repository
* ``git log`` shows a list of all previous commits

### Initialize

``git init`` to turn the current, empty directory into a fresh Git repository.
``echo "Hello Git and GitHub" >> README.txt`` to create a new README file (more on this later) with some sample text.
``git add README.txt`` to add the new file to the Git staging area.
``git commit -m "First commit"`` to make your first commit with the new README file.
``git push origin master`` to repo

### head commit
In Git, the commit you are currently on is known as the HEAD commit. In many cases, the most recently made commit is the HEAD commit.
```
git show HEAD
```
The output of this command will display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

### git checkout
What if you decide to change the ghost’s line in the working directory, but then decide you wanted to discard that change?

You could rewrite the line how it was originally, but what if you forgot the exact wording? The command
```
git checkout HEAD filename
```
will restore the file in your working directory to look exactly as it did when you last made a commit.

### Add multiple files 
```
more git add
```
### git reset I
Great! The files you’ve added to the staging area belong in the same commit.

What if, before you commit, you accidentally delete an important line

We can unstage that file from the staging area using
```
git reset HEAD filename
```
This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.

### git reset II
Creating a project is like hiking in a forest. Sometimes you take a wrong turn and find yourself lost.

Just like retracing your steps on that hike, Git enables you to rewind to the part before you made the wrong turn. You can do this with:
```
git reset commit_SHA
```

This command works by using the first 7 characters of the SHA of a previous commit. For example, if the SHA of the previous commit is 5d692065cf51a2f50ea8e7b19b5a7ae512f633ba, use:
```
git reset 5d69206
```
HEAD is now set to that previous commit.
* ``git checkout HEAD filename``Discards changes in the working directory.
* ``git reset HEAD filename`` Unstages file changes in the staging area.
* ``git reset commit_SHA`` Resets to a previous commit in your commit history.


 
 
