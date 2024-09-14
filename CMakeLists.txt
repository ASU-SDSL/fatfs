add_library(FatFs INTERFACE)

add_compile_definitions(DFF_USE_STRFUNC=1)

target_sources(FatFs INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/source/ffsystem.c
    ${CMAKE_CURRENT_LIST_DIR}/source/ffunicode.c
    ${CMAKE_CURRENT_LIST_DIR}/source/ff.c
    # ${CMAKE_CURRENT_LIST_DIR}/source/diskio.c
)

target_include_directories(FatFs INTERFACE
    source
    include
)
