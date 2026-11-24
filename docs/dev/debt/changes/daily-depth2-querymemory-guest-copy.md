# libSceDepth2

## add Functional

- [sceDepth2QueryMemory](../../../core/libs/prx/libSceDepth2/Export.cpp) (libSceDepth2) - reads `param` and writes `mem` through guest copies; an unreadable `param` or unwritable `mem` returns `0x80BB000A`, the code of a null pointer. The error for a non-null unmapped pointer is not measured on a console
