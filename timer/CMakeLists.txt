# Distributed under the Boost Software License, Version 1.0.
# See http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 2.8.8)

include(Ryppl)

ryppl_project(BoostTimer
  DEPENDS
    BoostChrono
    BoostConfig
    BoostSystem
)

if (${RYPPL_BoostTimer_VALID})

include_directories(include)

add_library(boost_timer
  src/auto_timers_construction.cpp
  src/cpu_timer.cpp
  )

target_link_libraries(boost_timer
  boost_chrono
)

endif()

ryppl_export(
  TARGETS
    boost_timer
  DEPENDS
    BoostChrono
    BoostConfig
    BoostCore
    BoostInteger
    BoostSystem
    BoostUtility
  INCLUDE_DIRECTORIES
    include
  )
