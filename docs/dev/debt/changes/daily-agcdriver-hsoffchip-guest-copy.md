# libSceAgcDriver

## add Functional

- [sceAgcDriverGetHsOffchipParam](../../../core/libs/prx/libSceAgcDriver/State/src/Configuration.cpp) (libSceAgcDriver) - writing the granularity and buffering through `GuestCopyOut_nid_no_patch` and throwing on an unwritable output is a host-safety fallback; the firmware faults on those pointers instead and its behaviour is not measured on a console.
