add_subdirectory(utils)

set(tango_const_h ${CMAKE_CURRENT_BINARY_DIR}/tango_const.h)
configure_file(tango_const.h.in ${tango_const_h})
set(COMMON_HEADERS
    ${tango_const_h}
    git_revision.h
)
install(FILES ${COMMON_HEADERS} DESTINATION "${CMAKE_INSTALL_INCLUDEDIR}/tango/common")
