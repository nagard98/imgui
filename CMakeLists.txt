cmake_minimum_required(VERSION 3.12)

project(imgui)

add_library(imgui STATIC imgui.cpp imgui.h imgui_demo.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp imconfig.h imgui_internal.h imstb_rectpack.h imstb_textedit.h imstb_truetype.h
    backends/imgui_impl_dx11.cpp backends/imgui_impl_dx11.h
    backends/imgui_impl_win32.cpp backends/imgui_impl_win32.h)

target_include_directories(imgui
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/backends
)
