cmake_minimum_required(VERSION 3.8)

file(GLOB IMGUIZMO_SRC CMAKE_CONFIGURE_DEPENDS *.h  *.cpp)

add_library(ImGuizmo STATIC ${IMGUIZMO_SRC})
set_target_properties(ImGuizmo PROPERTIES
	CMAKE_CXX_STANDARD 20
)
target_link_libraries(ImGuizmo PUBLIC imgui)
target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
