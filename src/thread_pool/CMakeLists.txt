cmake_minimum_required(VERSION 3.12.1)
SET(THREAD_POOL_NAME thread_pool)
MESSAGE(aaaa ${THREAD_POOL_NAME})
SET(THREAD_POOL_SRCLIST
        include/thread_pool/thread_pool.h
        thread_pool.cpp)

ADD_LIBRARY(${THREAD_POOL_NAME} ${THREAD_POOL_SRCLIST})
find_package(Threads)
target_link_libraries(${THREAD_POOL_NAME} ${CMAKE_THREAD_LIBS_INIT})