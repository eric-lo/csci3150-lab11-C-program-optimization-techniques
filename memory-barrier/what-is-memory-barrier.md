# What is memory barrier? {#shared-memory}

A memory barrier, also known as a _membar_, _memory fence_ or _fence instruction_, is a type of barrier instruction that causes a central processing unit \(CPU\) or compiler to enforce an ordering constraint on memory operations issued before and after the barrier instruction. This typically means that operations issued prior to the barrier are guaranteed to be performed before operations issued after the barrier.

Memory barriers is necessary sometimes because optimizations performed by the compiler and hardware can cause memory to be accessed in a different order than intended by the developer.

A memory barrier affects instructions that access memory in two ways:

* provides control over the order that memory access instructions are performed, and
* provides control over when memory access instructions will complete.



