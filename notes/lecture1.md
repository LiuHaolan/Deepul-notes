# Lecture 1

## Likelihood-based Model
estimating p<sub>data</sub> from samples x<sup>(1)</sup>, ... x<sup>(n)</sup> ~ p<sub>data</sub>(x)

Learns a distribution that can:

(1) **Inference**: given input x, output the probability p(x)

(2) **Sampling**: sampling arbitrary x ~ p(x)

## Historgram

(1) counting
Using a histogram with each bin for every possible samples, using frequency counting for each bins. Then inference is a directory lookup, and sampling becomes uniform sampling in the CDF. 

Drawback: For a D dimension vector, binarized representation, We need 2<sup>D</sup> bins! Very few data compared to the large numbers of bins.

(2) parameterized representation
Using a functional approximation model p<sub>theta</sub>(x).
Training data forms a log likelihood Sum(log(p<sub>theta</sub>(x<sup>i</sup>)), treat this as a loss function and use optimizer such as SGD to train.

Drawback: the output probability for every possible samples need to be normalized, i.e. for every possible x<sup>i</sup>, sum(p<sub>theta</sub>(x<sup>i</sup>)=1, and also every probability needs to be positive.
Such attributes are tricky to find.

## Autoregressive Model

### Masked Autoencoder

Using autoencoder as a generative model:


Motivation: 
