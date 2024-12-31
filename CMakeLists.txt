cmake_minimum_required(VERSION 3.8)

file(GLOB_RECURSE SRC CMAKE_CONFIGURE_DEPENDS *.h *.cpp)

add_library(ImGuizmo STATIC ${SRC})
set_property(TARGET ImGuizmo PROPERTY CXX_STANDARD 20)
target_link_libraries(ImGuimzo PUBLIC ImGui)
