# TLdgaHomology

WHAT IS THIS CODE: This code computes the homology groups of the complex of planar loops with ground ring the integers and parameter zero, using the minimal model (ADD REF ONCE ARXIVED) established in joint work in progress with Rachael Boyd, Oscar Randal-Williams, and Robin Sroka. It was written while we were halfway through writing that paper. We subsequently noticed that with parameter zero the homology is equivalently Ext over a truncated divided power algebra (ADD REF ONCE ARXIVED). From this point of view, the code is computing these Ext groups direct from the cobar complex, which probably isn't the most efficient method. Since this code already existed, I'm recording it here, together with some outputs (in the data folder).

PRECISELY: Work over Z, and let A_n be the truncated divided power algebra A_n=\Gamma_R[y]/(y^{[i]}, i \geq n+1), regarded as bigraded by setting y^{[i]} =(2i-1,i). The code computes the bigraded Ext^{A_n}(R,R) directly using the reduced cobar complex. In light of (ADD REF ONCE ARXIVED) this is equivalently the homology of a Temperley--Lieb algebra over Z with parameter 0 on an even number of strands 2n. 

WRITTEN IN: Python, as a jupyter notebook, using sage, numpy and scipy (the latter two to do sparse matrix computations), especially the homology functionality in sage - thanks to the developers!

HOW TO USE: The code has comments, which are numerous but not necessarily helpful. Basically, you set the two numbers at the top (n and maxDegree), then run all three blocks. The output you actually want is the last block, which gives some bigraded homology groups. The n is the n above, maxDegree is really the largest tensor power in the cobar complex where you compute everything, so you'll get all of the homology groups H_{d,w} where 2w-d \leq maxDegree (if it doesn't crash first).
  - If you want to write the homology you computed to a txt file, then there should be a folder called "data" in the same place as the code: this is where the outputs will go.
  - If you just want to print the output in your notebook, then you can comment out all of the file writing stuff with no ill effects.
How big you can make n and maxDegree will depend on how beefy your computer is: the outputs I'm including in the data file were obtained on an unremarkable laptop.

OBSERVATIONS ABOUT THE OUTPUTS: Non-simple torsion seems to be comparitively rare in low degrees: the smallest n for which the code found any is n=6 (2n=12), where H_{13,8} is Z \oplus C4.

ACKNOWLEDGEMENTS: Thanks to Christian Carrick and Charlotte Summers for various helpful pointers about the right way to do the code, and to use git.

FEEDBACK: Welcome, at guy.boyde@gmail.com.
