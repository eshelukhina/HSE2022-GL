set(BASE_SRCS
    GLWindow.cpp
    GLWindow.hpp
)
set(CMAKE_PREFIX_PATH "/usr/local/Cellar/qt@5/5.15.6")

add_library(Base ${BASE_SRCS})

find_package(Qt5 COMPONENTS Widgets REQUIRED)

target_link_libraries(Base
    PRIVATE
        Qt5::Widgets
)

add_library(FGL::Base ALIAS Base)