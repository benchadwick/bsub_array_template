# bsub_array_template

###########
##Purpose##
###########

This 'oneliner' for loop optimizes high-throughput batch submission of a directory of files for a given executable program in a Platform LSF HPC cluster environment utilizing a regular expression to enhance portability.

########
##Code##
########

for file in ~/bash_final/dir1/; do bsub -P acc_BSR1015F2015 -q expressalloc -W 2 -o ${file##/}.out -e ${file##/}.err -J ${file##/} cat ~/bash_final/dir1/${file##*/}; done
