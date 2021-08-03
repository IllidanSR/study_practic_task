cmake_minimum_required(VERSION 3.7)

project(My_awesome_app
        VERSION 0.0.0
        DESCRIPTION "My first awesome C++ application"
        LANGUAGES CXX
        )

add_subdirectory(src)
add_subdirectory(app)

if((CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME OR MODERN_CMAKE_BUILD_TESTING)
        AND BUILD_TESTING)
    enable_testing()
    add_subdirectory(tests)
endif()



