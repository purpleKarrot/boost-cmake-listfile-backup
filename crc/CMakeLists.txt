# Distributed under the Boost Software License, Version 1.0.
# See http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 2.8.8)

include(Ryppl)

ryppl_project(BoostCRC)

ryppl_add_test_subdirectory(test)

ryppl_export(
  DEPENDS
    BoostArray
    BoostConfig
    BoostCore
    BoostInteger
    BoostMPL
  INCLUDE_DIRECTORIES
    include
)
