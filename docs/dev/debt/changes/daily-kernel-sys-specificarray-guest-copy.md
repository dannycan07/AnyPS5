# libkernel_sys

## change [pthread_get_specificarray_np]

- [pthread_get_specificarray_np](../../../core/libs/prx/libkernel_sys/Export.Discovery.cpp) (libkernel_sys) - returns EINVAL (22) for non-positive total, key below 1 or key range exceeding 512, EFAULT (14) for null output or an output array that cannot be written, and otherwise copies thread-specific data via scePthreadGetspecific through `GuestCopyOut_nid_no_patch` while preserving `errno`. These argument checks and the 512-key bound are an unverified host model, and the console result for an unwritable array was not independently measured.
