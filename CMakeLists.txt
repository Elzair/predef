cmake_minimum_required(VERSION 3.3)

project(boost_predef)

add_library(boost_predef INTERFACE)

target_include_directories(boost_predef BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_predef DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::predef ALIAS boost_predef)
