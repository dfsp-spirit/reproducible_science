# Introduction: towards reproducible science using version control and GNU R

A very short introduction. 
https://tinyurl.com/repsci

## Reproducible science


**Reproducibility** is "the ability to recompute data analytic results given an observed dataset and knowledge of the data analysis pipeline" ([Leek & Peng 2015](https://www.pnas.org/content/112/6/1645.short))


## How can we get there?

Quoting (Leek & Peng 2015):

* "the raw data from the experiment are available"
* "the statistical code and documentation to reproduce the analysis are available"
* "correct data analysis must be performed"

Today, we will focus on the second point and explore tools which can help others to understand and reproduce your data analysis.

Note that *others* may include yourself, 2 months later. ;)

## Tools we will get to know:

* The version control system [Git](./git_intro/git_intro.md)
* Two R packages that help with reproducible research:
  * [apaTables](http://htmlpreview.github.io/?https://github.com/dfsp-spirit/reproducible_science/blob/master/apaTables_intro/r_apaTables_intro.html)
  * [rmarkdown](http://htmlpreview.github.io/?https://github.com/dfsp-spirit/reproducible_science/blob/master/rmarkdown_intro/rmarkdown_intro.html)

## Getting the latest version

You can get the latest version via git:

    git clone https://github.com/dfsp-spirit/reproducible_science.git

If you already have a copy of the repo, just refresh it from time to time:

    cd reproducible_science/
    git pull
