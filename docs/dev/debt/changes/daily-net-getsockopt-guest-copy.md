# libSceNet

## add Functional

- [sceNetGetsockopt](../../../core/libs/prx/libSceNet/Export.cpp) (libSceNet) - reading the option length and writing the option value and length through `GuestCopyIn_nid_no_patch` and `GuestCopyOut_nid_no_patch`, returning `-1` with `NET_EFAULT` on inaccessible guest pointers, is a host-safety fallback; the firmware's result for such pointers is not measured on a console.
