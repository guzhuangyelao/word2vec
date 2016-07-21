cmake_minimum_required(VERSION 2.8)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3 -march=native -Wall -funroll-loops -Wno-unused-result")

link_libraries(libm.a
    pthread)

add_executable(word2vec word2vec.c)
add_executable(compute-accuracy compute-accuracy.c)
add_executable(word2phrase word2phrase.c)
add_executable(distance distance.c)
add_executable(word-analogy word-analogy.c)