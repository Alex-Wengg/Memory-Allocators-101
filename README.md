# Memory-Allocators-101
Learning about memory allocation from this site:
https://arjunsreedharan.org/post/148675821737/memory-allocators-101-write-a-simple-memory

![image](https://user-images.githubusercontent.com/36247722/233709691-7441cab4-b793-43c6-97ff-1de4f581c3bb.png)

the data, bss and heap sections are collectively referred to as the “data segment”, 
brk: points to end of heap segmentation
Text section: The part that contains the binary instructions to be executed by the processor.
Data section: Contains non-zero initialized static data.
BSS (Block Started by Symbol) : Contains zero-initialized static data. Static data uninitialized in program is initialized 0 and goes here.

```
Calling sbrk(0) gives the current address of program break.
Calling sbrk(x) with a positive value increments brk by x bytes, as a result allocating memory.
Calling sbrk(-x) with a negative value decrements brk by x bytes, as a result releasing memory.
On failure, sbrk() returns (void*) -1.
```
