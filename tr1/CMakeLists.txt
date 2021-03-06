# Distributed under the Boost Software License, Version 1.0.
# See http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 2.8.8)

include(Ryppl)

ryppl_project(BoostTR1)

ryppl_add_doc_subdirectory(doc)

ryppl_export(
  DEPENDS
    BoostArray
    BoostBind
    BoostConfig
    BoostCore
    BoostFunction
    BoostFunctionalHash
    BoostFusion
    BoostIterator
    BoostMPL
    BoostMath
    BoostRegex
    BoostSmartPtr
    BoostStaticAssert
    BoostTuple
    BoostTypeTraits
    BoostUnordered
    BoostUtility
  RECOMMENDS
    BoostRandom
  INCLUDE_DIRECTORIES
    include
  )
