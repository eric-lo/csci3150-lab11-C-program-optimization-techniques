# Pin pages {#mmap}

We use the function **get\_user\_pages\_fast **to pin user pages in memory, the arguments needed are as follows:



```c
int get_user_pages_fast(unsigned long start, int nr_pages, int write, struct page ** pages)
```



where **unsigned long start** is the starting user address, **int nr\_pages** is the number of pages from start to pin, **int write** indicates whether pages will be written to, and **struct page \*\* pages** is the array that receives pointers to the pages pinned which should be at least **nr\_pages **long.

This function returns the number of pages pinned. This may be fewer than the number requested. If **nr\_pages **is 0 or negative, returns 0. If no pages were pinned, returns -errno.

