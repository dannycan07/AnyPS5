# libSceAppContent

## add Silent stubs

- [sceAppContentGetPftFlag](../../../core/libs/prx/libSceAppContent/Export.cpp) (libSceAppContent) - returning `SCE_APP_CONTENT_ERROR_PARAMETER` for an unwritable pft flag pointer is a host-safety fallback with console behavior unmeasured.
