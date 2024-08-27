cmake_minimum_required( VERSION 3.16 )

include(cmake/GitProjectVersion.cmake)

project( T8CODE_ADAPTIVE_RES
    DESCRIPTION "AMR data structures to switch between different resolutions of data adaptively and fast"
    LANGUAGES C CXX 
    VERSION "${ADAPTIVERESOLUTION_VERSION_MAJOR}.${ADAPTIVERESOLUTION_VERSION_MINOR}.${ADAPTIVERESOLUTION_VERSION_PATCH}"
)
include (CTest )

find_package(T8CODE)

include(CMakeDependentOption)

set( CMAKE_C_STANDARD 11 )
set( CMAKE_C_STANDARD_REQUIRED ON )
set( CMAKE_C_EXTENSIONS OFF )

set( CMAKE_CXX_STANDARD 17 )
set( CMAKE_CXX_STANDARD_REQUIRED ON )
set( CMAKE_CXX_EXTENSIONS OFF )

option( ADAPTIVE_RES_BUILD_AS_SHARED_LIBRARY "Whether Adaptive_Resolution should be built as a shared or a static library" ON )

add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/src )