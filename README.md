# bsub_array_template

###########
##Purpose##
###########

This 'oneliner' for loop optimizes high-throughput batch submission of a directory of files for a given executable program in a Platform LSF HPC cluster environment utilizing a regular expression to enhance portability.

########
##Code##
########

for file in ~/your_working_dir/; do bsub -P account -q que -W estimated_wall_time -o ${file##/}.out -e ${file##/}.err -J ${file##/} cat ~/your_working_dir/${file##*/}; done
