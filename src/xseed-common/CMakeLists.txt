CONFIGURE_FILE(${CMAKE_CURRENT_SOURCE_DIR}/config.h.in
        ${CMAKE_CURRENT_BINARY_DIR}/config.h)

add_sources(xseed-common display_help.c display_version.c generate_getop_options.c
            expand_array.c file_exists.c file_length.c regular_file.c
            get_dirname.c cat_strings.c)

IF (MSVC)
    add_sources(xseed-common unix_functions_for_windows.c)
ENDIF (MSVC)
