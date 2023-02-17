cmake_minimum_required(VERSION 3.10)
set(CMAKE_PREFIX_PATH "C:\\Qt\\5.15.2\\mingw81_64\\")
set(Qt5Widgets_DIR "C:\\Qt\\5.15.2\\mingw81_64\\bin\\")
set(Qt5_DIR "C:\\Qt\\5.15.2\\mingw81_64\\lib\\cmake\\Qt5\\")
project(Qt-CMake-HelloWorld)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

include_directories("C:\\Qt\\5.15.2\\mingw81_64\\include\\")
find_package(Qt5 COMPONENTS Core Widgets Gui REQUIRED)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${Qt5Widgets_INCLUDE_DIRS})

# set(CMAKE_AUTOMOC ON)
# set(CMAKE_AUTOUIC ON)
# set(CMAKE_AUTORCC ON)


add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE Qt5::Widgets Qt5::Core Qt5::Gui)
