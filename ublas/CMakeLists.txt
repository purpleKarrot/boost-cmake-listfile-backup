# Distributed under the Boost Software License, Version 1.0.
# See http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 2.8.8)

include(Ryppl)

ryppl_project(BoostUBLAS)

ryppl_export(
  DEPENDS
    BoostConceptCheck
    BoostConfig
    BoostMPL
    BoostSmartPtr
    BoostStaticAssert
    BoostTypeTraits
    BoostTypeof
    BoostUtility
  RECOMMENDS
    BoostSerialization
  INCLUDE_DIRECTORIES
    include
  )
