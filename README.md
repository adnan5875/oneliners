# oneliners
linux one liners

to delete files with prefix in the directory
rm -rf slurm-*

To delete files with particular strings in the directory
find . -iregex ".*\(_asrout\)\.\(rds\)" -delete
find . -iregex ".*\(_asrout\|_job-info\)\.\(rds\|out\)" -delete # you can provide or options as well


#To find files with particular extensions in directories and subdirectories and delete them
find . -type f -name slurm-\* -delete


#slurm jobs
to cancel slurm job using slurm job id
 squeue -u $USER | grep 20582305 | awk '{print $1}' | xargs -n 1 scancel
