

# Rising Sun Envelope Method

This is a companion repository for the paper  


**The Rising Sun Envelope Method: an automatic and accurate peak location technique for XANES measurements,**

by __R. Monteiro (MathAM-OIL/AIST, Sendai, Japan), I. Miyazato, and K. Takahashi (Hokkaido University, Japan).__ (published by  <a href=https://pubs.acs.org/doi/10.1021/acs.jpca.9b11712>The Journal of Physical Chemistry A</a>, DOI: 10.1021/acs.jpca.9b11712)

 All the code for that paper is available in this github in the folder "XANES-jupyter-notebook", in Python.

The method is based on a very on an old  lemma of Riesz, the  <a href="https://en.wikipedia.org/wiki/Rising_sun_lemma">Rising Sun Lemma</a>, used to study pointwise properties of functions, like its oscillations; we  use a similar construction to understand the oscillation seen in XANES measurements, "regularizing" the XANES measurement by constructing sequences of what we call Rising Sun functions in domains that are nested and smaller, leading to an iterated sequence of similar problems.


![An example of the Rising Sun Envelope Method in practice](https://github.com/rafael-a-monteiro-math/Rising_Sun_Envelope_Method/blob/master/docs/xanes-optimize.gif)

If you cite this work, please use the following piece of code:

```
@article{doi:10.1021/acs.jpca.9b11712,
author = {Monteiro, Rafael and Miyazato, Itsuki and Takahashi, Keisuke},
title = {Rising Sun Envelope Method: An Automatic and Accurate Peak Location Technique for XANES Measurements},
journal = {The Journal of Physical Chemistry A},
volume = {124},
number = {9},
pages = {1754-1762},
year = {2020},
doi = {10.1021/acs.jpca.9b11712},
note ={PMID: 32013431},
URL = {https://doi.org/10.1021/acs.jpca.9b11712},
eprint = {https://doi.org/10.1021/acs.jpca.9b11712}
}
```
## How this jupyter-notebook is divided

There are many auxiliary functions necessary for this code, therefore we begin by explaining them; afterwards we do the decomposition and finally we run the dimension reduction and interpolations.


## Further comments
<blockquote>There are many steps in the code that can be optimized. Indeed, we carried out many brute-force searches in a "careless", non-optimal way. For someone who might use this code in a daily basis, improving such property will make the difference between a code that runs in minutes rather than hours. Please, write, improve, and make our code better. We are advocating for a new idea with this method, and we believe - in fact, we are sure - that there is still a lot to be improved. 
</blockquote>


## Parts where we think the code can be improved
  <blockquote>
 <ol>
<li> Definitely, the plateau search can be improved: it doesn't need to return only one location, but it can return all the plateau locations</li>
<li>The code can be improved to deal with non-noise functions. The main modification should be inserted in the peak finding function: whenever there is a plateau, the function should allow the 0 index to be the location of the peak. This will create an inconvenient of either repeating indices, but there is a simple fix to that, which was not necessary in our case. </li>
  </ol>
</blockquote>


