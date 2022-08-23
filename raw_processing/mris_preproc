export SUBJECTS_DIR=/mnt/data/subjects
export FREESURFER_HOME=/mnt/data/soft/freesurfer
export FSFAST_HOME=/mnt/data/soft/freesurfer//fsfast
export FSF_OUTPUT_FORMAT=nii.gz
export MNI_DIR=/mnt/data/soft/freesurfer//mni

# mris_preproc resamples the data to the fsaverage template in mni space
# --fsgd fsgd file containing labels and covariates for each subj
# --target template to resample
# --hemi which hemi to resample
# --meas which structural measurement
# --out label for the output file

for hemi in lh rh 
do
	srun export SUBJECTS_DIR=/mnt/data/subjects ; 
	export FREESURFER_HOME=/mnt/data/soft/freesurfer ;
	source /mnt/data/soft/freesurfer/SetUpFreeSurfer.sh ; 
	/mnt/data/soft/freesurfer/bin/mris_preproc --fsgd exemple_fsgd.txt \
	--target fsaverage \
	--hemi $hemi \
	--meas pial_lgi \
	--out $hemi.lgi.mgh
done
