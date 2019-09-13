

# Rising Sun Envelope Method

This is a companion repository for the paper  <h>Decomposing XANES  spectral measurements using the Rising Sun envelope method</h>, by R. Monteiro, I. Miyazato, and K. Takahashi. All the code for that letter is here.

The method is based on a very on an old  lemma of Riesz, the Rising Sun Lemma (https://en.wikipedia.org/wiki/Rising_sun_lemma), used to study pointwise properties of functions, like its oscillations.  We use a similar construction to understand the oscillation seen in XANES, using it to "regularize" the XANES measurement by creating sequences of what we call Rising Sun functions in domains that are nested and smaller, leading to a sequence of smaller problems.




If you cite this work, please use the following piece of code. 


# Comments:

There are many steps in the code that can be optimized: there are many brute-force searches that were carried out in a "careless", non-optimal way, and for someone who might use this code in a daily basis this will make the difference between a code that runs in minutes rather than hours. Please, write, improve, and make our code better. We are advocating for a new business here, and we think that there is still a lot to be improved. 

## Parts where we think the code can be improved:

1. Definitely, the plateau search can be improved: it doesn't need to return only one location, but it can return all the plateau locations
2. The interpolation can be improved, and other types of interpolations are possible; for instance, by using clamped splines in each domain. 


## How is this notebook divided

There are many auxiliary functions necessary for this code, therefore we begin by explaining them; afterwards we do the decomposition and finally we run the dimension reduction and interpolations.

[[https://github.com/rafael-a-monteiro-math/RisingSunMethod-XANES-dimension-reduction/blob/master/XANES_with_marked_peaks_average-middle_step.png|alt=octocat]]

