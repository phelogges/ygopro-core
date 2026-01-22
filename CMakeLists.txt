project (ocgcore)

file(GLOB SRC_FILES "*.h" "*.cpp")

add_library (${PROJECT_NAME} STATIC ${SRC_FILES})

target_include_directories(${PROJECT_NAME} PRIVATE ${LUA_INCLUDE_DIR})

target_link_libraries(${PROJECT_NAME} PRIVATE ${LUA_LIBRARIES})

# Expose public include directory
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
