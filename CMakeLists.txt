cmake_minimum_required(VERSION 3.15)
project(22s_pa03)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS_RELEASE -O3)

add_executable(pa03 src/main.cpp src/Graph_helper.cpp)
configure_file(data/test_data_2.graphml data/test_data_2.graphml COPYONLY)
configure_file(data/dataset.graphml data/dataset.graphml COPYONLY)
configure_file(data/test_data_1.graphml data/test_data_1.graphml COPYONLY)
configure_file(data/test_data_3.graphml data/test_data_3.graphml COPYONLY)
configure_file(data/community_report.txt data/community_report.txt COPYONLY)
configure_file(data/football.graphml data/football.graphml COPYONLY)
configure_file(data/random_data_1.graphml data/random_data_1.graphml COPYONLY)
configure_file(data/random_data_2.graphml data/random_data_2.graphml COPYONLY)
configure_file(data/random_data_3.graphml data/random_data_3.graphml COPYONLY)
configure_file(data/random_data_4.graphml data/random_data_4.graphml COPYONLY)
configure_file(data/random_data_5.graphml data/random_data_5.graphml COPYONLY)
configure_file(data/random_data_6.graphml data/random_data_6.graphml COPYONLY)





set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)

find_package(Boost 1.71.0 REQUIRED COMPONENTS graph system filesystem)
message(STATUS "Boost version: ${Boost_VERSION}")

target_link_libraries(pa03 PUBLIC Boost::graph PUBLIC Boost::system PUBLIC Boost::filesystem)
