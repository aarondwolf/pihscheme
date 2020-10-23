# scheme-pih

---

## Quick Start Guide

The Partners in Health (PIH) Stata scheme provides a quick set of options for modern-looking graphs from Stata using PIH colors. The scheme is intended for use by the PIH data teams across sites when designing visualization for presentations and social media.

## Stata Installation

### Installing via *net install*

The current version is still a work in progress. To install, user can use the net install command to download from the project's Github page:

```
net install scheme-pih, from("https://aarondwolf.github.io/scheme-pih")
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

### Fonts

The scheme does not require or utilize any special fonts. Fonts can be edited to use PIH-standard fonts if the user so wishes with the following commands:

```stata
graph set window fontface <font-name>
graph set window fontfacemono <font-name>
graph set window fontfacesans <font-name>
graph set window fontfaceserif <font-name>
graph set window fontfacesymbol <font-name>
```


## Attribution

The PIH scheme was written by Aaron Wolf. Bugs can be reported via the repository at Github (https://github.com/aarondwolf/scheme-pih). Questions can be directed to aaron [dot] wolf [at] yale [dot] edu. 

This scheme used the user-written scheme *cleanplots* as a base, with alterations made to reflect Yale's colors and stylistic preferences. *cleanplots* was created by Trenton Mize, and documentation can be found at https://www.trentonmize.com/software/cleanplots. *cleanplots* was itself influenced by Daniel Bischof's very excellent *plotplain* scheme, documentation for which can be found at https://www.stata-journal.com/article.html?article=gr0070. 
