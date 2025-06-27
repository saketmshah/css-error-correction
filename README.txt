The attached Jupyter notebook includes a project on quantum error correction. 
The error code used is a particular CSS code, associated to the following generator matrix:

[[1,0,1,0,1,0,1,0,1,0,1,0,1,0,1], 
[0,1,1,0,0,1,1,0,0,1,1,0,0,1,1], 
[0,0,0,1,1,1,1,0,0,0,0,1,1,1,1], 
[0,0,0,0,0,0,0,1,1,1,1,1,1,1,1]]

A broad overview of the code is as follows: 
We use Gottesmann's algorithm (https://arxiv.org/pdf/quant-ph/9705052) to produce the 
logical all-zero state associated to this CSS code. We then apply a Pauli error with
a fixed probability p on each physical qubit. Afterwards, we measure ancillas and 
apply the appropriate error corrections. We then test the circuit by examining how it 
performs for different values of p, and how successful it is at correcting the errors.

Finally, for fun we test the output of (one implementation of) the Pauli error channel.