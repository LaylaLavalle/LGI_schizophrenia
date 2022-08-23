1) MrisPreproc.sh: The preprocessing file is not including any smoothing step as LGI data are already smooth (the degree of smoothness of the LGI data corresponds to a smoothing kernel of 10 mm). 
2) glm.sh: We need the z.mgh or sig.mgh file for our meta-analysis
3) ClusterCorr.sh: We don't use the correction for multiple comparison for our meta-analysis. We're correcting when computing linear regression analyses.
