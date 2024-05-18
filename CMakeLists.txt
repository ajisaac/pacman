cmake_minimum_required(VERSION 3.28)
project(pacman)
set(CMAKE_CXX_STANDARD 23)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
add_executable(pacman main.cpp )

include_directories(pacman "/opt/homebrew/Cellar/sdl2_image/2.8.2_1/include/SDL2")
target_link_libraries(pacman ${SDL2_LIBRARIES} "-L/opt/homebrew/Cellar/sdl2_image/2.8.2_1/lib -lSDL2_image")
