set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "Toolbox package used by Belldonne Communications projects")
set(CPACK_PACKAGE_VENDOR "Belledonne Communications")
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/../COPYING")
set(CPACK_PACKAGE_NAME ${PACKAGE})
set(CPACK_PACKAGE_VERSION_MAJOR ${PACKAGE_VERSION_MAJOR})
set(CPACK_PACKAGE_VERSION_MINOR ${PACKAGE_VERSION_MINOR})
set(CPACK_PACKAGE_VERSION_PATCH ${PACKAGE_VERSION_PATCH})

set(CPACK_RPM_COMPONENT_INSTALL OFF)

set(CPACK_COMPONENTS_ALL runtime devel)
set(CPACK_COMPONENT_DEVEL_DEPENDS runtime)
set(CPACK_COMPONENT_RUNTIME_DISPLAY_NAME ${PACKAGE})
set(CPACK_COMPONENT_DEVEL_DISPLAY_NAME ${PACKAGE}-devel)

if ("${CPACK_GENERATOR}" STREQUAL "RPM")
  set (CPACK_PACKAGE_FILE_NAME ${CPACK_PACKAGE_NAME}-${PACKAGE_VERSION})
endif ()

INCLUDE(CPack)
