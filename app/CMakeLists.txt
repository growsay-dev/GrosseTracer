add_executable(${PROJECT_NAME} main.cpp ${SOURCES})

find_package(Vulkan REQUIRED)
target_include_directories(${PROJECT_NAME} PUBLIC ${Vulkan_INCLUDE_DIRS})

target_link_libraries(${PROJECT_NAME} ${Vulkan_LIBRARIES} glfw)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/executables)