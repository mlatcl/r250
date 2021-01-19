---
layout: home
title: R250 Unsupervised Gaussian Processes
tagline: Neil Lawrence's notes for R250 Gaussian Process Course
hide: true
---

This is the material for my R250 Unit in 2020-2021 Academic Year on "Unsupervised Gaussian Processes".

### Introduction Session 

You can find the [intro talk and notes here](/r250/lectures/01-unsupervised-gaussian-processes.html).

Also there's a video of me giving [similar material at the Machine Learning Summer School here](http://inverseprobability.com/talks/notes/gaussian-processes.html).

If you want to review some of the background then the following might also be useful.

1. [Linear Algebra & Regression](http://inverseprobability.com/mlai2015/2015/10/13/week-3-linear-algebra-and-regression.html) from my old Sheffield Course (with [Jupyter notebook](https://nbviewer.jupyter.org/github/lawrennd/mlai2015/blob/master/week3.ipynb) and [video](https://www.youtube.com/watch?v=5VPr6NbHHjg)). 
2. [Bayesian Regression](http://inverseprobability.com/mlai2015/2015/11/03/week-6-bayesian-regression.html) from my old Sheffield course (also with [Jupyter notebook](https://nbviewer.jupyter.org/github/lawrennd/mlai2015/blob/master/week6.ipynb) and [video](https://www.youtube.com/watch?v=17zr5dGcUzE)) goes through some other important fundamentals like Bayes rule and multivariate Gaussians.
3. [Gaussian Processes]((/r250/lectures/01-gaussian-processes-intro.html) lecture from R250 in 2019-2020.

Here are the papers for the different sessions.

[Non-linear Matrix Factorization with Gaussian Processes](https://dl.acm.org/doi/10.1145/1553374.1553452) ICML 2009 with [Raquel Urtasun](http://www.cs.toronto.edu/~urtasun/)

[Metrics for Probabilistic Geometries](https://dl.acm.org/doi/10.5555/3020751.3020834) with [Alessandra Tosi](https://www.robots.ox.ac.uk/~atosi/index.html), [
‪Søren Hauberg‬](http://www2.compute.dtu.dk/~sohau/), [Alfredo Vellido](https://www.cs.upc.edu/~avellido/)

[Bayesian Gaussian Process Latent Variable Model](http://proceedings.mlr.press/v9/titsias10a.html) AISTATS 2010 with [Michalis K. Titsias](http://www2.aueb.gr/users/mtitsias/)

[Manifold Relevance Determination](https://dl.acm.org/doi/10.5555/3042573.3042644) ICML 2012 with [Andreas Damianou](https://adamian.github.io/), [Carl Henrik Ek](http://carlhenrik.com/), [Michalis K. Titsias](http://www2.aueb.gr/users/mtitsias/)

[Variational Learning of Inducing Variables in Sparse Gaussian Processes](http://proceedings.mlr.press/v5/titsias09a.html) AISTATS 2009 by Michalis Titsias

For some background, you can also check the first part of these [notes and video from the machine learning summer school in Stellenbosch](http://inverseprobability.com/talks/notes/deep-gaussian-processes.html). 

[Gaussian Processes for Big Data](http://www.auai.org/uai2013/prints/papers/244.pdf) UAI 2013 by James Hensman, Nicolò Fusi and Neil D. Lawrence.

[Deep Gaussian Processes](http://proceedings.mlr.press/v31/damianou13a.html) AISTATS 2013 by Andreas Damianou and Neil D. Lawrence.
 
For more background, check the second part of these [notes and video from the machine learning summer school in Stellenbosch](http://inverseprobability.com/talks/notes/deep-gaussian-processes.html). 

[Linear Latent Force Models using Gaussian Processes](http://eprints.whiterose.ac.uk/120149/1/1107.2699v1.pdf) by Mauricio Alvarez, David Luengo and Neil D. Lawrence in TPAMI.


### Session 1 

#### 1st February 2021 at 14:00 on Zoom


### Session 2 

#### 8th February 2021 at 14:00 on Zoom

 
### Session 3 

#### 15th February 2021 at 14:00 in Zoom


### Mini Project

For the mini-project I recommend one of four tasks.

1. Find an implementation of Bayesian GP-LVM and one of standard GP-LVM (for example in [GPy](https://github.com/SheffieldML/GPy). Explore different initialisation strategies. See how they compare for the Bayesian and non Bayesian approach. **Note**: for the Bayesian approach you will need an additional initialisation strategy around the variances of the posterior approximation for $\mathbf{X}$ so you might need several Bayesian GP-LVM comparisons. Explore the results for several different standard data sets. You could use simulated data and real data. You might want your exploration to be two stage. One where you keep covariance function parameters fixed, and one where you vary the covariance function parameters. 

2. Find an implementation of SVI for GPs. For a smaller dataset (where the standard sparse GP can also be used) explore the stochastic optimization routine. Try different patterns of update between the inducing variables and the covariance parameters. If possible, attempt to update the inducing point locations. Monitor the quality of results by comparing to the best-approximate GP as computed by the Titsias variational approach.

3. Use an implementation of Deep GPs to test different initialisation approaches. The implementation from my MLSS talk uses PCA for initializing latent spaces. What other approaches can you try?

4. Reimplement the latent force model covariance function in python. Be careful about numerical problems that arise in that reimplementation. Use your implementation to fit the latent force model to e.g. a small motion capture data set.
