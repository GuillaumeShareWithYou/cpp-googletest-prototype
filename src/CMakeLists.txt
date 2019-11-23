set(BINARY ${CMAKE_PROJECT_NAME}_lib)

set(MAIN Main.cpp)
# source files
file(GLOB SOURCES
    "*.cpp"
)

# Build a library with all project sources
add_library(Personne-lib  ${SOURCES})
## Create an executable with the main function
add_executable(${BINARY} ${MAIN})
# link the whole project sources lib to the main function
target_link_libraries(${BINARY} PUBLIC
Personne-lib)

include_directories(${CMAKE_SOURCE_DIR}/include)