# my_singularity

Create Ubuntu container from docker image:

    sudo /usr/local/bin/singularity bootstrap ubuntu16.img ubuntu16.def

Create Fedora container from docker image in sandbox:

    mkdir /local/scratch/containers
    sudo /usr/local/bin/singularity build --sandbox /local/scratch/containers/fedora27 fedora27.def

Bind a directory of choice to an image:

    sudo /usr/local/bin/singularity shell -w fedora27.img
    mkdir /local/scratch # inside container
    exit                 # inside container 
    sudo /usr/local/bin/singularity shell -w --bind /local/scratch fedora27.img

The directory creation can be done when building the image, no?


