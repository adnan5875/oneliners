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
 squeue -u $USER | grep 20582305 | awk '{print $1}' | xargs -n 1 cancel



To remove all the files in a folder “OUTPUT’ 

for year in {2013..2022}; 

 do   rm ./$year/OUTPUT/*;  

done 

 

# find all the files in a folder with desired extension and then add deleted to remove files 

find . -name "*.log" -type f 

find . -name "*.log" -type f -delete 

find . -name "*.out" -type f 

find . -name "*.out" -type f -delete 

 

find -type d -name "output" -exec rm -r {} + 

 

To make all folders and files open access 

chmod -R 777  /group/grains/pulses/adnan/chickpea_acidtol
