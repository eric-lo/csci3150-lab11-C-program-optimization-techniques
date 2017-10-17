# Memory barrier example {#shared-memory}

When a program runs on a computer with only one CPU, the necessary bookkeeping to used to ensure that the program is executed as if all memory operations were performed in the order specified by the programmer, so memory barriers are not necessary. However, when the program is executed in a multiprocessor system, then out-of-order access may affect the actual output of the program.

The following is a simple example showing a print program run in a two-CPUs system.

![](/assets/noMemoryBarrierCase.png)

The shared memory locations _flag \_and \_x_ both initialized to be 0. In the first processor, the program waits the variable flag to be non-0 and then print _x_, while in the second processor, the processor stores the value "100" into _x_ and "1" into _flag_. One may expect the print result is always "100"; however, if the operations of processor 2 are out-of-order, it is possible that flag is updated before x, so the print result might therefore be "0". Similarly, it is possible that in processor 1, the print statement can be executed before flag is checked, therefore the checking statement is out of effect here. So we need to add two memory barriers statements to make sure the program is run with the expected order, as illustrated as follows.

![](/assets/memoryBarrierCase.png)

After inserting the memory barriers, the print result will always be "100", as expected.

