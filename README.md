# Table of Contents
[Issue 1: ExFAT mounts in READ-only Mode](#issue-1-exfat-mounts-in-read-only-mode)

## Issue 1: ExFAT mounts in READ-only Mode
To fix it:</br>
1. Run `diskutil list` in the terminal, and find the name of the ExFAT disk. It ends with a pattern close to `s1` (e.g., `disk4s1`).
2. Unmount the drive by running `sudo umount /dev/disk4s1`
3. Make a directory in the `Volumes` dir: Run `sudo mkdir -p /Volumes/YOUR_DESIRED_DRIVE_NAME`
4. Mount the drive in the newly created volume: `sudo mount_exfat /dev/disk4s1 /Volumes/YOUR_DESIRED_DRIVE_NAME`

## Issue 2: Installing Tensorflow and Pytorch (without GPU)

1. Make a new conda environment based on python 3.8
2. Run `conda install -c conda-forge tensorflow`
3. Run `conda install -c pytorch pytorch`
4. Run `conda install jupyter`
5. Run `conda install nb_conda_kernels`
