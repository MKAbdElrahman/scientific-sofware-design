cmake_minimum_required(VERSION 3.25)
project(scientific-sofware-design 
LANGUAGES CXX
VERSION 0.1
HOMEPAGE_URL https://github.com/MKAbdElrahman/scientific-sofware-design
)


add_library(fdtd)
target_sources(fdtd PUBLIC src/fdtd.cpp)
target_compile_features(fdtd PUBLIC cxx_std_20)
target_include_directories(fdtd PRIVATE src PUBLIC include)
set_target_properties(fdtd PROPERTIES VERSION ${PROJECT_VERSION} SOVERSION ${PROJECT_VERSION_MAJOR})


add_subdirectory(test)
