## Table of Contents
[Issue 1: ExFAT mounts in READ-only Mode](#)

## Issue 1: ExFAT mounts in READ-only Mode
To fix it:</br>
1. Run `diskutil list` in the terminal, and find the name of the ExFAT disk. It ends with a pattern close to `s1` (e.g., `disk4s1`).
2. Unmount the drive by running `sudo umount /dev/disk4s1`
3. Make a directory in the `Volumes` dir: Run `sudo mkdir -p /Volumes/YOUR_DESIRED_DRIVE_NAME`
4. Mount the drive in the newly created volume: `sudo mount_exfat /dev/disk4s1 /Volumes/YOUR_DESIRED_DRIVE_NAME`
