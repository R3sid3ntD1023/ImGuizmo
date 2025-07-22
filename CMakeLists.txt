cmake_minimum_required(VERSION 3.10)

find_package(imgui CONFIG REQUIRED)

set(IMGUIZMO_SOURCES
   ${CMAKE_CURRENT_SOURCE_DIR}/ImGuizmo.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/ImSequencer.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/ImCurveEdit.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/GraphEditor.cpp
   ${CMAKE_CURRENT_SOURCE_DIR}/ImGradient.cpp
)


add_library(ImGuizmo STATIC ${IMGUIZMO_SOURCES})
add_library(ImGuizmo::ImGuizmo ALIAS ImGuizmo)

target_compile_definitions(ImGuizmo PUBLIC IMGUI_API)
target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(ImGuizmo PUBLIC imgui)
target_compile_definitions(ImGuizmo PUBLIC _CRT_SECURE_NO_WARNINGS)

