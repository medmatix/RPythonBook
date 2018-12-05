## Front Material

## Colophon

<h1 style="text-align:center;">R to Python</h1>
<h2 style="text-align:center;">Thoughts of an R programmer Learning Python</h2>

![Janus](Janus-iStock-494706611alpha.png)

<h4 style="text-align:center;">by David A York</h4>
   
  
     
   
Copyright 2018 David A York

http://crunches-data.appspot.com/contact.html 

This manuscript may be freely copied and distributed, under the MIT Licence

self-published, on Toth-York Imprint, Calhoun GA USA, November 27, 2018 

https://github.com/medmatix/RtoPythonThoughts 
  


___

>"In ancient Roman religion and myth, Janus (/ˈdʒeɪnəs/; Latin: IANVS (Iānus), pronounced [ˈjaː.nus]) is the god of beginnings, gates, transitions, time, duality, doorways,[1] passages, and endings. He is usually depicted as having two faces, since he looks to the future and to the past." 
>from Wikipedia, https://en.wikipedia.org/wiki/Janus, accessed 27 November, 2018 at 4:17PM
  
  
  
  
 
## Preface

This book is a work in progress on the thoughts of an R programmer (the author) moving to (or learning) Python. It is intended as a comparison of R and Python for those already using R. The hop is to ease the way for those in particular newer to programming as opposed to the quick task oriented scripting which R lends itself so well to. 

As with any language the most visible presence on line are the hardened champions of the languages with the pressure to standardization (not a bad thing per-se) and dogmatic adherence to the "blah blah" way of doing things (which is desirable I think).

Having started as an R user, then as an R programmer, I have relatively recently embarked on learning python as well. Why I would do this is rather complicated to explain, particularly as I had knowledge of other general programming languages, which would conceivably serve such a role, particularly BASIC and Java. Suffice to say that as a budding Data Scientist I see lots of reasons to know both R and Python. BASIC, though still extant it is very limited in support and relevant libraries by comparison. Java . . .  well, as a strong open source advocate I feel Java is bound to Oracle in many ways for all time. It is likely they have no intention of truly releasing it into the public domain, ever. There is far more rationel to learn C++ these days than Java for the sake of what is arguably only minor difference in learning curve.

I absolutely love R! When I returned to school to study Applied Math and Statistics it was an ever present partner for me. It could do most things I needed, though matrix math was less smooth than Matlab the price was right (not withstanding Octave or Scilab). However, I increasingly found the need for a general purpose programming language and Python was there growing in the guise of 'the' data science alternative.

But while R was great with vectorized functions python, at it's core, was weak in this regard. The libraries for python have been growing steadily in number and variety, and the functionality gap between it and R narrows in cluding for vectorized application. I still cannot see a Data Scientist being as productive not knowing R at this point. However, I see no reason not to also know Python - ergo, I think any serious Data Science needs to know both; AND, there is the added incentive of the interoperability of R and Python (and C++)! From R we have [XRPython](https://cran.cnr.berkeley.edu/web/packages/XRPython/index.html) and [reticulate](https://cran.cnr.berkeley.edu/web/packages/reticulate/index.html) and from Python we have [Rpy2](https://rpy2.bitbucket.io/).

The Organization of the book is in 2 parts. A close Comparison and discussion of R and Python unburdened with a mandate to teach beginning programming in either. The is overview of part 1, I only touch quite generally on the nature of the usual programming sturctures. Variables, datatypes and data structures, binary decisions, repeating code blocks and so are part of all declarative or functional programming language - the rest is just details. The Same can be side for laguages introducing object-oriented programming models.

In the second part of the book, an opportunity is taken to compare how data science is done in R and Python in the various domains we work.

One could consider this as a second source for R users learning python, after the beginner courses to get the python syntax vocabulary.


# Introduction

Learning a new programming or scripting language begs comparison. Often this is not overly helpful to the learner who, coming from a zone of comfort is often frustrated by old subtleties not consciously recognized, being yet unknown in the new. I recall a family member, completely new to computers, saying why doesn't it know what I mean expecting the implied parts of language to transfer from English (or German, or Chinese etc.) to computer language.

R writers early on recognize the absence of vectorization of functions in core python. It's available though in numpy and pandas, but base python doesn't have it and they miss it. You'll get there, really. Object Orientation is also not natural to either R or Python. It came later to both, but it seems more smoothly accomplished by python than R.

I soon realized, though that you had to know the programming commonalities of python first; R comparisons really should start with the libraries of python. R in someways has cut right to the data science chase often at the expense of strong programming constructs. This is the nod to interactive coding and scripting rather than the need to undertake formal programming. Python began early on with a scripting functionality but it wasn't until the development of iPython the interactive python could be realized in the way that R users were used to.

All this is not to say that R was lacking in basic programming constructs from the start, it wasn't; but he proportion of users who used R in a quick-and-dirty small problem focused way was very high. This suited it's use in a statistical learning environment.  I should think that those who try to start python at the same time as their first statistics course will find the learning curve too steep to help with the statistics part of the need.

# A Comparative Look



As already mentioned, it is not the intent of this treatise to teach either beginning R or python scripting. There are many good sources for this and yet another beginners book or tutorial is, I believe, not needed. For ease of reference I include  [Appendix1](https://github.com/medmatix/RtoPythonThoughts/blob/master/Appendix_1.md) as an overview of relevant R and python syntax for the general programming constructs any functional language. In Part 1, at the risk of being pedantic, I am simply giviing a fairly generic overview of the components of the typical script or program as a framework to be used in organizing our R and Python comparisons.

## Functional Programming Commonalities.

In functional programming operational code is incorporated by task and purpose into blocks of code which are called by name in the body of a script. This usually includes some connecting statemts and assignments which cause the functions to operate together to accomplish some larger task.

Historically, Fortran and Basic code in common accademic and educational use, became unwieldy as users became, more and more, writers of rampant spagetti code.The introduction of the concept of 'structured programming' and the uniform reliance on subroutine and function call tamed the spagetti-monster. Extension to functional programming with pascal and modern C was a natural extension of this trend.

So the reliance of R and Python on script collections of functions calling each other is what we are at now. Functions are subprograms that have all the statement tasks common to most programs. I will deal in a general way with these statement types and include comparsions between how R and Python each express the tasks. It is not the intent of this book to actually teach beginning programming as previously mentioned. Consult the bibliography for some suggested sources for peginning programmers.

The later innovation of object oriented programming concepts evolving from this will be touched on in a comparative fashion in another chapter.

### Statements and Expressions

A program or script is of course considered as a series of statement stored together. These statements constitute expressions of mathemetical equations (see specifically [Chapter 5]()), choices, and other orders to be carried out by the machine. 

With any program or script statements tasks and values stored are executed or accessed from memory locations. This was the innovation conceived of by John Von Neumann which moved programming from the moving wire jumpers to the input to the machine from various codes punched into tapes or cards to be held in memory while being used.

### Assignment of Values to Memory and the Variable

Variables are memory locations assigned values as the computing process goes on. The classification of specific locations determines a type of data held there.

The codes stored in the machine include a specific operator code to direct the move of a value received for input or a statement's result to a memory location. This is called and assignment. 

Traditionally R has used the combined dash-less-than symbols ' -> ' for this purpose but the simple equals sign ' = ' now also works in this fashion. Python uses the same equals sign for assignments.

Variables are named in both R and Python and neither may begin with a digit. There are other restrictions and conventions which are not gone into here. 


### Decisions and Choices

As currently implemented all choices by a computer resolve to yes or no results. Some semblance or the greys we think in are a result of a collection or range of yes-no questions. These choices are explicit of implicit 'if' queries.

### Doing it Over Again (and again ...)

Loops are created within a program logic, usually involving a choice test to be executed which cause tasks to be repeated zero or more times. It is considered bad parctice to create a loop without some form of exit (short of having to power down the machine).

### Functions 

Functions in fortran were short program clips that did a task and immediately returned a value . Subroutines are more like what functions in R and Python are, though returning to the calling place with some value is a frequent option with these functions as well. Functions may provide a new programming element like a square root (python, math.sqrt(x)) extending the language, or functions may carry out a whole task like carring out a liner regression, storing objects of the answer in memory for retrieval, or return as an object explicitly. Ofter a function is called that builds a whole grphic plot for display or other output when called.

In R,

```
function.name <- function(arguments) 
{
  computations on the arguments
  maybe other code too
}
```

and in Python indents take the place of brackets to define code blocks. Self in the function spec is the calling code block, and if omitted, is created by python implicitly. So, your first argument one way of another is the calling namespace. Self in the indented code block is the function itself.

```
def aroutine(self, args)
  computations on args
  maybe other code too
```

The notation of R is C (and Java) - like and Python is Pascal-like in format. Unlike pascal there is no 'begin:' keyword required at anytime in the script. 

Functional programming with R and Python, will be expanded on in it's own chapter later on.

### Objects and Classes

In general terms we will come to consider all program elements as objects. A Class will be considered as a pattern definition for an object. All objects are used as instances of some previously defined class. 
