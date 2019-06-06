# Introduction to Git

## What is Git?

[Git](https://git-scm.com/) is a *version control system*, i.e., a software that allows you to manage different versions of files in a repository.

The repository is a directory that is managed by git, and it can be on your computer or on a remote server.

Git can be used to:
* manage and access different versions of files
* work on the same set of (text) files with several (or *a lot* of) people and solve the resulting conflicts that may occur
* do many complex things which are specific to software development that we do not care about today

Git can help you to solve to the following problems:
* You messed up your R script today when working on it, and you want to get the version from yesterday back.
* You want to know the settings you used when computing the data for paper XY, but you have changed the script in the meantime.
* You want to see the changes introduced to a script since last month.
* Both you and a colleague made changes to the same script. You want to merge them to create a new version based on both change sets.
* You are working on a script over time, and you want colleagues to be able to access the latest version (without sending emails to them after every change)
* You want colleagues or others to be able to see your code, and maybe even allow them to directly make or suggest changes (which you can accept or refuse)

Git is **not**:
* An online document editor that allows several people to collaborate live on the same Word/Excel/whatever document
* A backup solution
* A direct replacement for file hosting or sharing services like DropBox


Alternatives to Git include [Mercurial](https://www.mercurial-scm.org/), [Darcs](http://darcs.net/), and [Apache Subversion](https://subversion.apache.org/).

## Some general tips

Things you should do:
* Separate data and code
* Commit often (several times per day, after every major change). It does not hurt and it ensures you always have the latest version available, should you need to continue working on another machine.
* write scripts in a machine-independent way

Things you should **not** do:
* Store credentials (passwords) in any Git repository
* Store copyrighted material you do not own, personal data, or patient data of any kind in a public Git repository
* Use git as a replacement for backups
* Check-in large data files
* Check-in files which can be easily generated from other files in the repo (e.g., you should add the Rmd file, but not the PDF, doc or html files which you can export based on the Rmd file)


## Let's get started

### Ensure your git installation works

First make sure you have [downloaded](https://git-scm.com/) and installed git. Just answer all questions with the default setting.

* Start a command line:
  * Windows: start *Programs* / *Git* / *Git Bash*
  * MacOS: in *Finder*, click *Applications* / *Terminal*
  * Linux: in the Start Menu, click *System Tools* / *xterm*

Now type `git --version`. You should see version information for git. If you get an error like `Command not found` instead, you either have not installed git or have not yet added it to your PATH environment variable. You will need to fix this before proceeding.

### Perform first-time setup

Note that these are **not** credentials for some remote server, they are just something to identify you when you add something to a repo. You can put whatever you want.

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"


### Create your first repo and add a file

Let's create a new repository:

    pwd
    mkdir myrepo
    cd myrepo
    git init

Now let us create a file named *README.md* in the repo and add it. You can use a text editor to create a file, or just use the command line:

    touch README.md
    git add README.md
    git commit -m "Add empty readme file"

It's time to make a change. Edit the file using a text editor and add a line, e.g., "# My public R project". Make sure to save the file. Now let us add the changed file.

    git status
    git add README.md
    git commit -m "Add basic info to readme file"
    git status

 We now have a second version of the file in the repo. Let's view the commit history:

     git log --oneline

 Note the commit hashes which are displayed. Let us jump back to an earlier version of the repo, identified by a commit hash:

     git checkout <hash>

 And return to the latest version again:

    git checkout master

## Alternatives to the command line

There are many [graphical user interfaces for git](https://git-scm.com/downloads/guis), and many advanced text editors (like [Atom](https://atom.io/)) and all major integrated development environments (IDEs, like rstudio, netbeans, pycharm, VSCode,...) have support for git.

## Getting a server

There are hosting platforms like github.com, gitlab.com or bitbucket.com which provide git hosting combined with a convenient web interface to browse files and revisions as well as other tools (e.g., project management or bug tracking software).

Most offer repos for free if you are working alone or in a small team, but for some free repos cannot be private.

## More info on git

* The official [git documentation website](https://git-scm.com/doc): great documentation, tutorials, videos, ...
* the [slides used for the course, from courses.cs.washington.edu](https://courses.cs.washington.edu/courses/cse403/13au/lectures/git.ppt.pdf)
  * License and credits for the linked presentation: *Portions of the CSE403 web may be reprinted or adapted for academic nonprofit purposes, providing the source is accurately quoted and duly creditied. The CSE403 Web: © 1993-2019, Department of Computer Science and Engineering, Univerity of Washington*


## Getting the latest version of this document

You can get the latest version via git:

    git clone https://github.com/dfsp-spirit/reproducible_science.git

If you already have a copy of the repo, just refresh it from time to time:

    cd reproducible_science/
    git pull
