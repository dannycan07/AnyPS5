# libSceAudioOut

## add Functional

- [sceAudioOutSetVolume](../../../core/libs/prx/libSceAudioOut/src/AudioOut.cpp) (libSceAudioOut) - reading the volume array through `GuestCopyIn_nid_no_patch` before any port volume changes, returning `-2144993276` while preserving `errno` on an inaccessible guest pointer, is a host-safety fallback; the firmware faults on that pointer instead and its behaviour is not measured on a console.
