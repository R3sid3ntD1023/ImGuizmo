cmake_minimum_required(VERSION 3.8)

file(GLOB IMGUIZMO_SRC CMAKE_CONFIGURE_DEPENDS *.h *.cpp)
find_package(imgui CONFIG REQUIRED)
add_library(ImGuizmo STATIC ${IMGUIZMO_SRC})
set_property(TARGET ImGuizmo PROPERTY CXX_STANDARD 20)
target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(ImGuizmo PUBLIC imgui)

