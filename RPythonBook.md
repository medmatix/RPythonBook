--- 
title: "R to Python"
description: R to Python, This is a bookbook in progress on the throughts of an R
  programmer moving to (or learning) Python.
documentclass: book
link-citations: yes
site: bookdown::bookdown_site
biblio-style: apalike
---



```{r echo=FALSE, include=FALSE}
# automatically create a bib database for R packages
knitr::write_bib(c(
  .packages(), 'bookdown', 'knitr', 'rmarkdown'
), 'packages.bib')
```

<!--chapter:end:index.Rmd-->

# Colophon

<h1 style="text-align:center;">R to Python</h1>
<h2 style="text-align:center;">Thoughts of an R programmer Learning Python</h2>
<img src="Janus-iStock-494706611alpha.png" alt="Janus, the Two-Faced God of Gateways">
<h4 style="text-align:center;">by David A York</h4>
   
  
     
   
Copyright 2018 David A York

This manuscript may be freely copied and distributed, under the MIT Licence

self-published, on Toth-York Imprint, Calhoun GA USA, November 27, 2018 
  
http://crunches-data.appspot.com/contact.html 

___

![Janus, Vatican Museum](220px-Janus1.JPG)

>"In ancient Roman religion and myth, Janus (/ˈdʒeɪnəs/; Latin: IANVS (Iānus), pronounced [ˈjaː.nus]) is the god of beginnings, gates, transitions, time, duality, doorways,[1] passages, and endings. He is usually depicted as having two faces, since he looks to the future and to the past." 

>from Wikipedia, https://en.wikipedia.org/wiki/Janus, accessed 27 November, 2018 at 4:17PM

<!--chapter:end:01-Cover.Rmd-->


# Preamble

## R to Python Thoughts

This book is a work in progress on the thoughts of an R programmer (the author) moving to (or learning) Python


## Introduction

Having started as an R user, then R programmer I have relatively recently embarked on learning python as well. Why I would do this is rather complex, particularly as I had other general programming languages I had learned, which would conceivably serve such a role, particularly BASIC and Java. Suffice to say that as a budding Data Scientist I see lots of reasons to know both R and Python, and BASIC though still extant is very limited in support and relevant libraries by comparison. Java, well, as a strong open source advocate I feel Java is bound to Oracle in many ways for all time. It is likely they have no intention of truly releasing it into the public domain, ever.

I absolutely love R! When I returned to school to study Applied Math and Statistics it was an ever present partner for me. It could do most things I needed, though matrix math was less smooth than Matlab the price was right. However, I increasingly found the need for a general purpose programming language and Python was there growing in the guise of 'the' data science alternative.

But while R was great with vectorized functions python, at it's core, was weak in this regard. The libraries for python have been growing steadily in number and variety, and the functionality gap between it and R narrows in cluding for vectorized application. I still cannot see a Data Scientist being as productive not knowing R at this point. However, I see no reason not to also know Python - ergo, I think any serious Data Science needs to know both; AND, there is the added incentive of the interoperability of R and Python (and C++)! From R we have [XRPython](https://cran.cnr.berkeley.edu/web/packages/XRPython/index.html) and [reticulate](https://cran.cnr.berkeley.edu/web/packages/reticulate/index.html) and from Python we have [Rpy2](https://rpy2.bitbucket.io/).

Chapter 1 of R to Python [here](https://github.com/medmatix/RtoPythonThoughts/blob/master/chapter_1.md) continues my Thoughts .


<!--chapter:end:02-preamble.Rmd-->

# A Comparative Look

Learning a new programming or scripting language begs comparison. Often this is not overly helpful to the learner who, coming from a zone of comfort is often frustrated by old subtleties not consciously recognized, being yet unknown in the new. I recall a family member, completely new to computers, saying why doesn't it know what I mean expecting the implied parts of language to transfer from English (or German, or Chinese etc.) to computer language.

R writers early on recognize the absence of vectorization of functions in core python. It's available though in numpy and pandas, but base python doesn't have it and they miss it. You'll get there, really. Object Orientation is also not natural to either R or Python. It came later to both, but it seems more smoothly accomplished by python than R.

I soon realized, though that you had to know the programming commonalities of python first; R comparisons really should start with the libraries of python. R in someways has cut right to the data science chase often at the expense of strong programming constructs. This is the nod to interactive coding and scripting rather than the need to undertake formal programming. Python began early on with a scripting functionality but it wasn't until the development of iPython the interactive python could be realized in the way that R users were used to.

All this is not to say that R was lacking in basic programming constructs from the start, it wasn't; but he proportion of users who used R in a quick-and-dirty small problem focused way was very high. This suited it's use in a statistical learning environment.  I should think that those who try to start python at the same time as their first statistics course will find the learning curve too steep to help with the statistics part of the need.

Now, it is not the intent of this treatise to teach either beginning R or python scripting. There are many good sources for this and yet another beginners book or tutorial is, I believe, not needed. For ease of reference I include [Appendix1](https://github.com/medmatix/RtoPythonThoughts/blob/master/Appendix_1.md) as an overview of relevant R and python syntax for the general programming constructs any functional language.

### Functional Programming Commonalities.




<!--chapter:end:03-chapter_1.Rmd-->

---

---

# Set-up for R and Python Exercises
  
Clearly you have to get R and python onto your system. R is available at the Comprehensive R Archive Network (CRAN) through it's many mirrors like [](https://cloud.r-project.org/) and Python through the [Python Software Foundation](https://www.python.org/). If you are doing a clean install of these I suggest installing [Anaconda,Python Data Science Platform](https://www.anaconda.com/) can make things much easier in the long run for integrating R and Python and Reproducible Research work. You can use [RStudio](https://www.rstudio.com/) or [Project Jupyter](http://jupyter.org/install) Notebook.

All of these sites will help you approach installs and configurations in a variety of ways. As an R programmer first I installed R then RStudio and then Python 3. This gave the maximum flexibility for R and Python in their own environments. I then did a parallel Anaconda install with R and RStudio and iPython for Jupyter Notebooks. This sets you up nicely for any approach to data science and development you could choose down the road.

You really are going to need an IDE for Python. [Spyder](https://www.spyder-ide.org/), available separately or installed through Anaconda is a solid python focused choice. I use [Eclipse](https://www.eclipse.org/) as you can use it for multiple languages including R (not as strong yet) and python. 

## Package Libraries

The strength of both R and Python is from their libraries. [CRAN Package  Repository](https://cran.cnr.berkeley.edu/index.html) and [Bioconnector](http://www.bioconductor.org/about/) are both well stocked with general and special purposed functions for R. RStudio develops [R Packages](https://www.rstudio.com/products/rpackages/) integrating well with the RStudio environment. The are lost of R packages in development awaiting addition to CRAN or hosted outside of CRAN such as on [Github](https://github.com/search?q=R+language).

If the reader has spent any time with R at all you have likely made inroads into these package sources. So how does Python compare? Python comes with a large standard library providing "out of the gate" functionality to compare with R-core. The best handing of the intricacies of the python standard library I've found is Doug Helmann's [The Python 3 Standard Library by example](https://amazon.com/Python-Standard-Library-Example-Developers/dp/0134291050/). Python Software foundation hosts the [Python Package Index , PyPi](https://pypi.org/) analygous to the CRAN repositories and Bioconnector. Also, the most important resource to get you up to speed is [SciPy tools](https://www.scipy.org/) consisting of SciPy, Numpy, Pandas and Matplotlib. These are the essential minimum to do any R-like work in python. These and more can be accessed as well through the [Numfocus Projects](https://numfocus.org/sponsored-projects). Finally, you have to check out the [StatsModels](https://www.statsmodels.org/stable/index.html) package site.

## Pulling it Together

Having apprised ourselves of the breadth and availability of these resources we will go forward and organize some of the ideas. R packages can be installed with the R GUI but the RStudio environment is much easier for this. Once a package is installed it is available in all environments I've alluded to. Compiling and installing is always best and I thing RStudio makes this fairly painless. Remember to start the GUI, Anaconda or RStudion environment as administrator to keep things together.

### Installing Packages

From the R GUI prompt we have,

```
  package-install()
```

Python packages from any source mentioned above can be installed with the PIP utility. This can be done from the shell prompt (remember to start as administrator or root):

```

  $ pip install matplotlib  
    # OR
  $ python -m pip install matplotlib

```

This can be done as root with the anaconda prompt as well.

### Using Packages

In R we must make sure the package (once installed) is loaded for our session. This is done with the library() function,

```
  library("MASS")
````

while in python we import the package previously installed as,

```
  import numpy
```

Once imported or loaded into either, we can access the functions of MASS directly by name. If we have a previous function of the same name it gets overwritten unless in python we keep the name spaces separate. This can be done by the form of the import statement. We can also import only slected functions from a package module.


```

  import numpy as np             # usual format to use namespace segregation of functions
  from numpy import sum, matrix  # economical import, still can conflick without use of as
  
```

<!--chapter:end:04-Chapter_2.Rmd-->

# Basic Arithmetic Comparison

This is pretty straight forward and intuitive stuff. Just the same, for completeness here it is.

## Add, Subtract, Multiply and Divide

### R Scripting




### Python Scripting


<!--chapter:end:05-Chapter_3.Rmd-->


# Functional Programming with R and Python

At this point we are ready to discuss the functional programming paradigm in R and Python. The other important paradigm, Object-Oriented, will be discussed in the following Chapter.

## Defining Functions

### R Scripting


### Python Scripting


## Calling and Using Functions

### R Scripting


### Python Scripting



## The Core or Standard Libraries

### R Scripting


### Python Scripting

<!--chapter:end:06-Functional_Programming.Rmd-->

# Using Probability Distributions with R and Python

At this point we are ready to discuss the functional programming paradigm in R and Python. The other important paradigm, Object-Oriented, will be discussed in the following Chapter.

## Basic Probability Issues

### R Scripting


### Python Scripting


## Using the Distrbutions

### R Scripting


### Python Scripting



## Other Libraries with Probability and Statistical Packages

### R Scripting


### Python Scripting

<!--chapter:end:07-Probability.Rmd-->


# Descriptive Statistics and Data Exploration

At this point we are ready to discuss the functional programming paradigm in R and Python. The other important paradigm, Object-Oriented, will be discussed in the following Chapter.

## Defining Functions

### R Scripting


### Python Scripting


## Calling and Using Functions

### R Scripting


### Python Scripting



## The Core or Standard Libraries

### R Scripting


### Python Scripting

<!--chapter:end:08_DescandExploration.Rmd-->


# Statistical Analysis and Modeling

At this point we are ready to discuss the functional programming paradigm in R and Python. The other important paradigm, Object-Oriented, will be discussed in the following Chapter.

## Defining the Available Functions

### R Scripting


### Python Scripting


## Calling and Using Functions

### R Scripting


### Python Scripting

<!--chapter:end:09_StatAnalModels.Rmd-->

# Object-Oriented Programming with R and Python

At this point we are ready to discuss the functional programming paradigm in R and Python. The other important paradigm, Object-Oriented, will be discussed in the following Chapter.

## Defining Classes

### R Scripting


### Python Scripting


## Using Objects and Classes

### R Scripting


### Python Scripting



<!--chapter:end:11-OO_Programming.Rmd-->

# Appendix 1

## Comparative Syntax for Programming Constructs of R and Python

As introduced in the text, the syntax of both R and python for the basic programming constructs are reviewed there for reader convenience.


||R|Python|
|----------------|----------------------------|----------------------------------|
|Basic data types and structures |scalar == vector[0]|scalars|
||vectors, (numerical, character, logical, factor) |(string, integer, float)|
||arrays, == vectors (m x n)|arrays (m x n) of scalars|
||matrices, ||
||data frames, |dictionary,|
||and lists |and lists|
|Operators|||
|conditionals|||
|Loops|||
  
## Extended Structures
  

<!--chapter:end:12-Appendix_1.Rmd-->

---

---


# References

1. Core R Team (Ed) [R Reference Index](https://cran.cnr.berkeley.edu/doc/manuals/r-release/fullrefman.pdf), R Foundation for Statistical Computing, Vienna, 2018.

2. Hellmann, Doug, [The Python 3 Standard Library by example](https://www.amazon.com/Python-Standard-Library-Example-Developers-ebook/dp/B072QZZDV7), Addison-Wesley, Boston MA, 2017.

<!--chapter:end:13-References.Rmd-->

