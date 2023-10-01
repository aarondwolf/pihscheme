# pihscheme

---

## Quick Start Guide

The PIH Stata scheme provides a quick set of options for modern-looking graphs from Stata using Partners in Health (PIH) colors. The scheme is intended for use by the PIH data analysis teams across their sites when designing visualization for presentations and social media.

## Stata Installation

### Installing via *net install*

The current version is still a work in progress. To install, user can use the net install command to download from the project's Github page:

```
net install pihscheme, from("https://aarondwolf.github.io/pihscheme")
```

### Usage

To use, simply specify the scheme at the start of a .do file:

```
set scheme pih
```

Or in the process of making a graph:

```stata
sysuse auto
twoway  (scatter price mpg if foreign == 0) ///
		(scatter price mpg if foreign == 1), scheme(pih) 
```


## Attribution

The PIH scheme was written by Aaron Wolf. Bugs can be reported via the repository at Github ([https://github.com/aarondwolf/pihscheme](https://github.com/aarondwolf/pihscheme)). Questions can be directed to aaron [dot] wolf [at] u [dot] northwestern [dot] edu. 

This scheme used the user-written scheme *cleanplots* as a base, with alterations made to reflect PIH'scolors and stylistic preferences. *cleanplots* was created by Trenton Mize, and documentation can be found at https://www.trentonmize.com/software/cleanplots. *cleanplots* was itself influenced by Daniel Bischof's very excellent *plotplain* scheme, documentation for which can be found at https://www.stata-journal.com/article.html?article=gr0070. 