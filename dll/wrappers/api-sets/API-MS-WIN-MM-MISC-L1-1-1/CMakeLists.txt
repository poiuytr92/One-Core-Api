
spec2def(API-MS-WIN-MM-MISC-L1-1-1.dll API-MS-WIN-MM-MISC-L1-1-1.spec)

list(APPEND SOURCE
    API-MS-WIN-MM-MISC-L1-1-1.rc
    ${CMAKE_CURRENT_BINARY_DIR}/API-MS-WIN-MM-MISC-L1-1-1_stubs.c
    ${CMAKE_CURRENT_BINARY_DIR}/API-MS-WIN-MM-MISC-L1-1-1.def)

add_library(API-MS-WIN-MM-MISC-L1-1-1 SHARED ${SOURCE})

set_module_type(API-MS-WIN-MM-MISC-L1-1-1 win32dll ENTRYPOINT 0)
add_importlibs(API-MS-WIN-MM-MISC-L1-1-1 winmm kernel32 ntdll)
add_dependencies(API-MS-WIN-MM-MISC-L1-1-1 psdk)
add_cd_file(TARGET API-MS-WIN-MM-MISC-L1-1-1 DESTINATION reactos/system32 FOR all)
