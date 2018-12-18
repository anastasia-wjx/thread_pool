CMAKE_MINIMUM_REQUIRED(VERSION 3.8.0)

SET(PJT_TEST_THREAD_POOL test_thread_pool)
SET(PJT_TEST_THREAD_POOL_SRCLIST
        main.cpp)


add_executable(${PJT_TEST_THREAD_POOL} ${PJT_TEST_THREAD_POOL_SRCLIST})
add_dependencies(${PJT_TEST_THREAD_POOL} thread_pool)
target_link_libraries(${PJT_TEST_THREAD_POOL} thread_pool)