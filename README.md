# Modelling sleep duration using Gaussian Processes

In this project I cluster users of wearable sensors based on their sleep duration
patterns. First, Gaussian Process (GP) models are fitted to users’ sleep duration
time series and parameters of fitted GP kernels are extracted for each user. These
parameters are consequently used to perform hierarchical clustering of users and to
interpret the discovered clusters. I compare two kernel types and several choices of
parameters used for clustering. My experiments show that the periodic GP kernel
is better suited for this problem than the product of Matérn and periodic kernel, and
that kernel parameters other than periodicity are not informative for the clustering.
My results reveal two main clusters of users who differ primarily in periodicity of
their sleeping patterns. Additionally, I provide extensive interpretation in terms of
other measures such as bed in and bed out times or number of steps. 
