# libSceFreeTypeOl

## add Driver removal and glyph-slot lifetime

- [sceFreeTypeOlAlloc](../../../core/libs/prx/libSceFreeTypeOl/ModuleWrappers.cpp) (libSceFreeTypeOl) - an unreadable memory record or an unwritable output pointer returns 6 (the existing invalid-argument result) instead of crashing the host, via `GuestCopyIn_nid_no_patch` / `GuestCopyOut_nid_no_patch` preserving host `errno`; the block is released through the record's `free` callback when the output cannot be written after allocation. This is a host-safety fallback; the console's result on invalid guest memory is unmeasured.
