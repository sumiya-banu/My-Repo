cmake_minimum_requried(VERSION 3.8)
set(This ExampleTests)
set(Sources 
    ExampleTests.cpp
    )

add_exeutable($(This) ${Sources})
target_link_libraries(${This} PUBLIC
    gtest_main
    Example
)  

add_test(
     NAME ${This}
     COMMAND ${This}
)