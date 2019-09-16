

# Rising Sun Envelope Method

This is a companion repository for the paper  


**The Rising Sun Envelope Method: an automatic and accurate peak location technique for XANES measurements,**

by __R. Monteiro (MathAM-OIL/AIST, Sendai, Japan), I. Miyazato, and K. Takahashi (Hokkaido University, Japan).__ (<a href=https://arxiv.org/abs/1909.06049>preprint arXiv, 2019</a>)

 All the code for that paper is available in this github, in Python.

The method is based on a very on an old  lemma of Riesz, the  <a href="https://en.wikipedia.org/wiki/Rising_sun_lemma">Rising Sun Lemma</a>, used to study pointwise properties of functions, like its oscillations; we  use a similar construction to understand the oscillation seen in XANES measurements, "regularizing" the XANES measurement by constructing sequences of what we call Rising Sun functions in domains that are nested and smaller, leading to an iterated sequence of similar problems.


If you cite this work, please use the following piece of code. 

<blockquote>
 <b>Comments:</b>
There are many steps in the code that can be optimized: there are many brute-force searches that were carried out in a "careless", non-optimal way, and for someone who might use this code in a daily basis this will make the difference between a code that runs in minutes rather than hours. Please, write, improve, and make our code better. We are advocating for a new business here, and we think that there is still a lot to be improved. 
</blockquote>

<blockquote>
  <b>Parts where we think the code can be improved:</b>
 <ol>
<li> Definitely, the plateau search can be improved: it doesn't need to return only one location, but it can return all the plateau locations</li>
<li>The code can be improved to deal with non-noise functions. The main modification should be interted in the find peak function: whenever there is a plateau, the function should allow the 0 index to be the location of the peak. This will create an inconvenient of either repeating indices. It is a simple fix, which was not necessary in our case. </li>
  </ol>
</blockquote>

## How is this notebook divided

There are many auxiliary functions necessary for this code, therefore we begin by explaining them; afterwards we do the decomposition and finally we run the dimension reduction and interpolations.

