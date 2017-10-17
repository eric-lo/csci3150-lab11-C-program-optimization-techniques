# Pin pages {#mmap}

We use the function **get\_user\_pages\_fast **to pin user pages in memory, the arguments needed are as follows:

_int get\_user\_pages\_fast\(unsigned long start, int nr\_pages, int write, struct page \*\* pages\),_

where _unsigned long start _is_ _the starting user address_, int nr\_pages_ is the number of pages from start to pin, _int write_ indicates whether pages will be written to, and _struct page \*\* pages_ is the array that receives pointers to the pages pinned which should be at least _nr\_pages _long.

This function returns the number of pages pinned. This may be fewer than the number requested. If _nr\_pages_ is 0 or negative, returns 0. If no pages were pinned, returns -errno.

