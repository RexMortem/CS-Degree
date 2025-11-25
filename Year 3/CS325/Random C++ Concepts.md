## Ownership 

Ownership is most simply defined as responsibility to cleanup. 

**Example:** So a block of memory can have multiple pointers pointing to it. One of these pointers may be designated as "owning" the block - this means it is responsible for cleaning up (deallocating/freeing) the memory. For instance, this clean up may happen when this owning pointer falls out of scope. 
## Smart Pointers

Smart pointers automatically manage deallocation (freeing memory) when pointers go out of scope. 

### Auto Pointer

auto_ptr is a smart pointer that takes [[#Ownership]] of the memory. The memory is deallocated when the auto_ptr falls out of scope.

**Warning:** Auto Pointer is deprecated after C++11 and is generally replaced by Unique Pointer.
### Unique Pointer

The wrapped pointer cannot be shared. Use move to transfer ownership. 