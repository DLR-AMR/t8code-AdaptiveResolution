cmake_minimum_required( VERSION 3.16 )

include(cmake/GitProjectVersion.cmake)

project( T8CODE_ADAPTIVE_RES
    DESCRIPTION "AMR data structures to switch between different resolutions of data adaptively and fast"
    LANGUAGES CXX 
    VERSION "${ADAPTIVERESOLUTION_VERSION_MAJOR}.${ADAPTIVERESOLUTION_VERSION_MINOR}.${ADAPTIVERESOLUTION_VERSION_PATCH}"
)
include (CTest )

find_package(T8CODE)