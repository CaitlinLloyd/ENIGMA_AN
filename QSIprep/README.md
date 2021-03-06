Recommendations for QSIprep

To run QSIprep, we recommend the following command:

qsiprep $BIDS_directory $output_directory participant -w $working_directory -l $log_file --output-resolution $voxel_dims --separate-all-dwis  --denoise-method none --unringing-method none --participant_label $name_of_sub --dwi_only --fs-license-file $path_to_fslicensefile --skip_bids_validation 

If an Nvidea GPU is available, you can speed up the processing using eddy_cuda. You would specify this option in an eddy_params file (see single shell and multi-shell options in eddy_files folder), adding this argument (--eddy-config $name_of_eddy_params_file) to the above line. The examples provided will implement slice to volume correction.

If a GPU is not available, the default eddy_params file will work just fine, and you do not need to modity eddy_params.

More information about QSIprep is available here: https://qsiprep.readthedocs.io/en/latest/usage.html#note-on-using-cuda
More information about FSLeddy (used for motion, Eddy current, and susceptibility distortion correction), including slice to volume correction is available here:
https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/eddy
