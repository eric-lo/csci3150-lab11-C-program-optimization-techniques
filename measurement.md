# Measurement of cache misses and TLB misses {#measurement-of-cache-misses-and-tlb-misses}

This part briefly describes how to measure cache misses and TLB misses:

* use [_perf_](https://perf.wiki.kernel.org/index.php/Main_Page) to access the hardware performance counters

**Important Note**:

Please run **perf** on department **linux9 **servers. Because VirtualBox can **NOT **support  **perf**  though  **perf**  can be installed on VM successfully.

You can follow the steps to connect the department linux9 servers:

* Download a SSH client and connect to the linux9 server. Here we use putty as an example.![](/assets/putty.png)

The host name is at the form of "username@linux9.cse.cuhk.edu.hk"

* Enter your password and you can connect to the department linux9 server.

![](/assets/linux9server.png)

* Remember to add "-std=c99" when compiling your program, for example:

```
gcc -std=c99 -o helloworld helloworld.c
```



