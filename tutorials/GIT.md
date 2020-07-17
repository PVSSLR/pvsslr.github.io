



## GIT Cheat Sheet 

## Version Control  

### Prerequisites

The prerequisites are given below
```
 A. Github, gitlab account 
 B. Git Bash
```
### Installing
Install Git Bash - [Click Here](https://git-scm.com/downloads) 
### GIT commands

Git is the industry-standard version control system for web developers
Use Git commands to help keep track of changes made to a project:

*  ``git init`` creates a new Git repository
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

### HEAD Commit
In Git, the commit you are currently on is known as the HEAD commit. In many cases, the most recently made commit is the HEAD commit.
```
git show HEAD
```
The output of this command will display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

### GIT Checkout
What if you decide to change the ghost’s line in the working directory, but then decide you wanted to discard that change?

You could rewrite the line how it was originally, but what if you forgot the exact wording? The command
```
git checkout HEAD filename
```
will restore the file in your working directory to look exactly as it did when you last made a commit.

### Add Multiple Files 
```
more git add
```
### GIT Reset I
Great! The files you’ve added to the staging area belong in the same commit.

What if, before you commit, you accidentally delete an important line

We can unstage that file from the staging area using
```
git reset HEAD filename
```
This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.

### GIT Reset II
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


 
### git branch

Up to this point, you’ve worked in a single Git branch called master. Git allows us to create branches to experiment with versions of a project. Imagine you want to create version of a story with a happy ending. You can create a new branch and make the happy ending changes to that branch only. It will have no effect on the master branch until you’re ready to merge the happy ending to the master branch.

In this lesson, we’ll be using Git branching to develop multiple versions of a resumé.

You can use the command below to answer the question: “which branch am I on?”
```
git checkout
```
Great! You just created a new branch.

The master and fencing branches are identical: they share the same exact commit history. You can switch to the new branch with
```
git checkout branch_name
```

### git branch

commit on a new branch
Congratulations! You have switched to a new branch. All the commands you do on master, you can also do on this branch.

For example, to add files to the staging area, use:

```
git add filename
```

And to commit, use:

```
git commit -m "Commit message"
```

In a moment, you will make a commit on the fencing branch. On the far right, the diagram shows what will happen to the Git project.


### git merge

What if you wanted include all the changes made to the fencing branch on the master branch? We can easily accomplish this by merging the branch into master with:

```
git merge branch_name
```

For example, if I wanted to merge the skills branch to master, I would enter

```
git merge skills
```

In a moment, you’ll merge branches. Keep in mind:

Your goal is to update master with changes you made to fencing.
fencing is the giver branch, since it provides the changes.
master is the receiver branch, since it accepts those changes.


### merge conflict I

The merge was successful because master had not changed since we made a commit on fencing. Git knew to simply update master with changes on fencing.

What would happen if you made a commit on master before you merged the two branches? 
Furthermore, what if the commit you made on master altered the same exact text you worked on in fencing? 
When you switch back to master and ask Git to merge the two branches, Git doesn’t know which changes you want to keep. 
This is called a merge conflict.

### delete branch

In Git, branches are usually a means to an end. You create them to work on a new project feature, but the end goal is to merge that feature into the master branch. After the branch has been integrated into master, it has served its purpose and can be deleted.

```
git branch -d branch_name
```

will delete the specified branch from your Git project.

Now that master contains all the file changes that were in fencing, let’s delete fencing.


``git clone`` Creates a local copy of a remote.
``git remote -v`` Lists a Git project’s remotes.
``git fetch `` Fetches work from the remote into the local copy.
``git merge origin/master`` Merges origin/master into your local branch.
``git push origin <branch_name>`` Pushes a local branch to the origin remote.
``git pull`` get data from repo