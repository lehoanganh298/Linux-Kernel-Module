## Linux Kernel Module 
Program create a Linux Kernel Module (LKM) that generate radom numbers. This LKM create a character device and allow user space processes to open and read random numbers that it generated.
### Referenced source:
* [Tutorial by Derek Molloy](http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction/)
* [Tutorial by Robert W. Oliver](https://blog.sourcerer.io/writing-a-simple-linux-kernel-module-d9dc3762c234)
### Install
1. Run `make`.
2. Insert kernel module: `sudo insmod randnum_char.ko`.
3. Run file test: `sudo ./test`.
4. Finish, remove the kernel module: `sudo rmmod randnum_char`
