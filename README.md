	This is simply a place where I will note down how I use Git so that I don't forget when I 
	inevitably leave it alone for a while.  If useful, feel free to fork and if you find anything 
	isn't correct, please fork, amend and push any corrections. Or, as sometimes there are simply 
	different styles rather than outright best practice, show me easier ways to do things. :-)
	I initially used an OpenDocument format for the file, but realised it didn't lend itself to 
	collaborative work so I converted it to a Markdown Readme file, which I love...

## How to Use Git and GitHub

Ian Till  -  December 2018

### Introduction
This is at least initially, a simple guide to the steps I went through to install Git on my laptop and get it running with a GitHub account to use repositories from all over the net.  My aim is mainly to be able to keep my stock of Arduino libraries up to date (which up until this point I have only downloaded as Zip files and extracted into my working folders.

A lot of the basic usage has been learned from this excellent video on YouTube from Sumit Kumar:  https://www.youtube.com/watch?v=ZrhdlerQ0rA 

Comments are welcome as I develop this, especially where I may inevitably make mistakes or misunderstand what is actually happening at the beginning.  If this is useful to anyone else, that's really great.  :-)

### Git and GitHub?

Git and GitHub sound like much the same thing and indeed they have similar functions in different places.  
- **Git** is the underlying tool that manages repositories of files with version control, supporting multiple concurrent users and allowing those users to operate on the same software at :he same time, then combine their work centrally in a managed workflow (process).  The Git application is generally installed on the User's computer and its function is simply to manage repositories and perform the various synchronisation actions between web copies, local copies and development branches.
- **GitHub** is an open, online web-based repository system where users can publish their files (code, images, data sets and even documents like this one).  A user can take someone else's work and build on it, improve or fix it and then offer those changes back to the original author, or simply build their own version and tailor it to their own needs.  As the original author improves their codes, GitHub also facilitates updating of derivatives (forks) and therefore benefits both authors and users.

### The Git Workflow

(insert diagram and describe)


### Installing Git

My machine is a an Acer Chromebook C720 running the excellent GalliumOS, essentially a lightweight version of Ubuntu.  These steps should broadly be good for any Debian based distro:

	sudo apt update
	sudo apt upgrade
	sudo apt-get install git-all

Once installed, configure a user:

	git config --global user.name "ian"
	git config --global user.email git@example.com

Check settings with:

	git config --list

Display help with:

	git help

or (e.g. for specific help with the add command):

	git add -h 

### Using Git on your local machine

Navigate to your chosen working folder on your machine in the terminal.

Create a local master level repository:

	git init

Create a file in the new folder, or if it already contains files and then add them all to the repository (start tracking them and stage them for commit):

	git add .
	
Or for a this single file:

	git add howToUseGit.md

Now commit them to the repository:
	
	git commit -m 'reason for the commit'   
	
The command above commits all the staged files, (the -m is a shortcut, enter the note of why the commit was made in single quotes).  Without the -m directive, you are presented with a text editor screen and must enter your commit notes into that before the commit will succeed.

To show the status of the current repository and all the files in it (whether the files are tracked, untracked or staged):

	git status

**Awesome... we've:**

- Created a new master repository,
- Added a new file to Git,
- Committed that file to the repository,
- Checked that the file has been committed.

**After this point, there are two obvious things to do:**

- Edit the file and commit the changes again,
- Link this local repository to an online one and push these changes to it,
- Branch this repository so that changes can be made in the branch and then reviewed before merging them with the master branch.

### Add a branch, select it, make edits, stage the changed files and commit...

Instructions here

### When done, merge the branch with the Master branch (or main line)...

Instructions here

### Create a new remote repository on GitHub
   git add myRepo https://github.com/abs-zero-ian/someRepo.git

### Create a new remote branch on GitHub
   git push -u origin new_branch_name
