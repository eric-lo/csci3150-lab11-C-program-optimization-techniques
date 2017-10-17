# Using Shared Memory in C {#using-shared-memory-in-c}

If you use the following functions in your program, you should link your program with`-lrt`.

If a process want to access shared memory, it should: \(use POSIX API\)

1.Create, or gain access to, a shared memory object.

```c
int shm_open (const char *name, int oflag, mode_t mode);
```

2.Map a shared memory object into its address space.

```c
void *mmap (void *addr, size_t length, int prot, int flags, int fd, off_t offset);
```

3.Do operations on shared memory \(read, write, update\).

4.Delete mappings of the shared memory object.

```c
int munmap (void *addr, size_t length);
```

1. Destroy a shared memory object when no references to it remain open.

```c
int shm_unlink (const char *name);
```



