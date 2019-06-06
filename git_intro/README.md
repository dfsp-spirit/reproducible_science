# Introduction to Git

## What is Git?

[Git](https://git-scm.com/) is a *version control system*, i.e., a software that allows you to manage different versions of files in a repository.

Git can be used to:
* manage and access different versions of files
* work on the same set of (text) files with several (or *a lot* of) people and solve the resulting conflicts that may occur (*cf* software development)
* do many complex things which are specific to software development that we do not care about today

In science, git provides solutions to the following problems:
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


## Let's get started

First make sure you have [downloaded](https://git-scm.com/) and installed git.

* Start a command line:
  * Windows: press *Windows+X* to open the Power Users menu, and then click *Command Prompt*
  * MacOS: in *Finder*, click *Applications* / *Terminal*
  * Linux: in the Start Menu, click *System Tools* / *xterm*

Now type `git --versions`. You should see version information for git. If you get an error like `Command not found` instead, you either have not installed git or have not yet added it to your PATH environment variable. You will need to fix this before proceeding.




## Materials

[the Presentation used for the course, from courses.cs.washington.edu](https://courses.cs.washington.edu/courses/cse403/13au/lectures/git.ppt.pdf)

License and credits for the linked presentation: Portions of the CSE403 web may be reprinted or adapted for academic nonprofit purposes, providing the source is accurately quoted and duly creditied. The CSE403 Web: © 1993-2019, Department of Computer Science and Engineering, Univerity of Washington
