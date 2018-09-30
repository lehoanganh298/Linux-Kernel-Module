## Linux Kernel Module 
Program create a Linux Loadable Kernel Module (LKM) that generate radom numbers. This LKM is a character device driver that allow user space processes to open and read random numbers that it generated through a device file.
### Referenced source:
* [Tutorial by Derek Molloy](http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction/)
* [Tutorial by Robert W. Oliver](https://blog.sourcerer.io/writing-a-simple-linux-kernel-module-d9dc3762c234)
### Files descriptions:
* randnum_char.c: code for create the character device driver as a LKM, with the read function generate and send a random number.
* test_randnum_char.c: code for create a user program that open and read the random number through the device file.
* Makefile: for build 2 files above and other necessary files.
### Install
1. Install Linux headers: `` sudo apt-get install build-essential linux-headers-`uname -r` ``
1. Build: `make`.
1. Insert kernel module: `sudo insmod randnum_char.ko`.
1. Run file test: `sudo ./test`. &larr; show the output with the random number read from the LKM
1. Finish, remove the kernel module: `sudo rmmod randnum_char`
