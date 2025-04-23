# TLdgaHomology

WHAT IS THIS CODE: This code computes the homology groups of the complex of planar loops with ground ring the integers and parameter zero, using the minimal model (ADD REF ONCE ARXIVED) established in joint work in progress with Rachael Boyd, Oscar Randal-Williams, and Robin Sroka. It was written while we were halfway through writing that paper. We subsequently noticed that with parameter zero the homology is equivalently Ext over a truncated divided power algebra (ADD REF ONCE ARXIVED). From this point of view, the code is computing these Ext groups direct from the cobar complex, which probably isn't the most efficient method. Since this code already existed, I'm recording it here, together with some outputs (in the data folder).

PRECISELY: Work over Z, and let A_n be the truncated divided power algebra A_n=\Gamma_R[y]/(y^{[i]}, i \geq n+1), regarded as bigraded by setting y^{[i]} =(2i-1,i). The code computes the bigraded Ext^{A_n}(R,R) directly using the reduced cobar complex.

WRITTEN IN: Python, using sage, numpy and scipy (the latter two to do sparse matrix computations), especially the homology functionality in sage - thanks to the developers!

ACKNOWLEDGEMENTS: Thanks to Christian Carrick and Charlotte Summers for various helpful pointers about the right way to do the code, and to use git.

FEEDBACK: Welcome, at guy.boyde@gmail.com.
