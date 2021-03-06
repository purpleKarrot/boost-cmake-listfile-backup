# Distributed under the Boost Software License, Version 1.0.
# See http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 2.8.8)

include(Ryppl)

ryppl_project(BoostFilesystem
  DEPENDS
    BoostSystem
)

if (${RYPPL_BoostFilesystem_VALID})

include_directories(include)

add_library(boost_filesystem
  src/operations.cpp
  src/path.cpp
  src/portability.cpp
  src/utf8_codecvt_facet.cpp
  src/codecvt_error_category.cpp
  src/path_traits.cpp
  src/unique_path.cpp
  src/windows_file_codecvt.cpp
  )

if(NOT BUILD_SHARED_LIBS)
  set_target_properties(boost_filesystem PROPERTIES
    PREFIX "lib"
    )
endif(NOT BUILD_SHARED_LIBS)

target_link_libraries(boost_filesystem
  boost_system
  )

boost_library_naming(boost_filesystem)

ryppl_add_test_subdirectory(test)

endif()

ryppl_export(
  TARGETS
    boost_filesystem
  DEPENDS
    BoostConfig
    BoostCore
    BoostFunctionalHash
    BoostIO
    BoostInteger
    BoostIterator
    BoostSmartPtr
    BoostStaticAssert
    BoostSystem
    BoostTypeTraits
    BoostUtility
  INCLUDE_DIRECTORIES
    include
  )
