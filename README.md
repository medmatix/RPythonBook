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


# [Introduction](_book/introduction.html)
