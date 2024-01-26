# add Library Automata_Lib
add_library(Automata_lib automaton.cpp)
# CMAKE_SOURCE_DIR is the top level folder in this case Automata_Example thats why we do /include
target_include_directories(Automata_lib PUBLIC ${CMAKE_SOURCE_DIR}/include)

# add executable 
add_executable(Automata_example main.cpp)
target_link_libraries(Automata_example PUBLIC Automata_lib)