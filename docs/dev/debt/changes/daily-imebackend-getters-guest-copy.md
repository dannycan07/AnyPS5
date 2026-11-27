# libSceImeBackend

## change [sceImeBackendGetCandidateList, sceImeBackendGetCandidateListSize, sceImeBackendGetCandidateSelect]

- [sceImeBackendGetCandidateList, sceImeBackendGetCandidateListSize, sceImeBackendGetCandidateSelect](../../../core/libs/prx/libSceImeBackend/Export.cpp) (libSceImeBackend) - the host backend has no conversion engine, so it reports an empty candidate list and selection zero for every input. The module builds candidates from its dictionaries and IPMI client, which are not modelled. `sceImeBackendGetCandidateSelect` and `sceImeBackendGetConvertMode` return 0x80bc1031 for an unwritable output pointer; the console's result for such a pointer is not measured.
