######################################################################
# Modelling Sleep Duration Using Gaussian Processes
# LE49: MiniProject
# Jan Ondras (jo356), Trinity College
# 2017/2018
######################################################################
# README
######################################################################

Filenames are mostly self-explanatory. 
The source code files form the following pipeline:

######################################################################
1.) ANALYSIS & PREPROCESSING

	user_means_distributions.ipynb
		For each user calculate mean of particular measure => show distributions.

	user_distributions.ipynb
		Visualise distributions of sleepduration/step count for various users INDEPENDENTLY; perform Normality test for sleep duration.

	daily_correlations.ipynb
		Show day-to-day correlations for sleepduration.

	sample_kernels.ipynb
		Sample kernels to see how kernel parameters affect the behaviour of functions obtained.

	extract_user_data.ipynb
		Extract (x,y) time series data for various datatypes (sleepduration, bed in, bed out times, step count), for each user. 
		Also perform data cleaning: remove measurements with sleepduration > 20 hours
		Also show few more stats - on weekly basis

######################################################################
2.) FITTING GP => GETTING KERNEL PARAMETERS

	fit_user_GP_sleepduration.ipynb
		For each user fit GP to sleepduration data and save extracted kernel parameters; 1264 users; both kernel types

######################################################################
3.) CLUSTERING KERNEL PARAMETERS

	cluster_params_periodicKernel.ipynb
		Perform hierarchical clustering using periodic kernel parameters. 
		For both variants: 4 params, or periodicity only.
		And interpret in terms of kernel parameters: mean trajectories, plots, ...

	cluster_params_productKernel.ipynb
		Perform hierarchical clustering using product kernel parameters. 
		For both variants: 5 params, or 2 only.
		And interpret in terms of kernel parameters: mean trajectories, plots, ...

	ARI_periodicKernel.ipynb
		Calculate Adjusted Rand Index for the 2 kinds of periodic kernel.

######################################################################
4.) INTERPRETATION OF CLUSTERS (in terms of other measures than kernel parameters)

	interpret_clustering.ipynb
		Extract all the statistics about discovered clusters.