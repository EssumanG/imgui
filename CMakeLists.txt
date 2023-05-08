cmake_minimum_required(VERSION 3.0)
project(IMGUI)

set(HEADERS "${IMGUI_SOURCE_DIR}/imconfig.h"
            "${IMGUI_SOURCE_DIR}/imgui.h"
            "${IMGUI_SOURCE_DIR}/imgui_internal.h"
            "${IMGUI_SOURCE_DIR}/imstb_rectpack.h"
            "${IMGUI_SOURCE_DIR}/imstb_truetype.h"
            "${IMGUI_SOURCE_DIR}/imstb_textedit.h")

set(SOURCES "${IMGUI_SOURCE_DIR}/imgui_demo.cpp"
            "${IMGUI_SOURCE_DIR}/imgui_draw.cpp"
            "${IMGUI_SOURCE_DIR}/imgui_tables.cpp"
            "${IMGUI_SOURCE_DIR}/imgui_widgets.cpp"
            "${IMGUI_SOURCE_DIR}/imgui.cpp")

# set(BACKEND_DIR "${IMGUI_SOURCE_DIR}/backends/imgui_impl_opengl3.cpp" 
#                 "${IMGUI_SOURCE_DIR}/backends/imgui_impl_opengl3.h"
#                 "${IMGUI_SOURCE_DIR}/backends/imgui_impl_glfw.cpp"
#                 "${IMGUI_SOURCE_DIR}/backends/imgui_impl_glfw.h")

add_library(imgui ${HEADERS} ${SOURCES} )

    target_compile_options(imgui PUBLIC -fPIC)

