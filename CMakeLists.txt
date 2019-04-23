cmake_minimum_required(VERSION 3.5.1)
project(robot_plan_runner)

set(CMAKE_CXX_STANDARD 11)

find_package(drake CONFIG REQUIRED)
#find_package(GFlags MODULE REQUIRED COMPONENTS shared)
find_package(Threads REQUIRED)
find_package(yaml-cpp REQUIRED)


add_executable(simple_continuous_time_system simple_continuous_time_system.cc)
target_link_libraries(simple_continuous_time_system drake::drake)
#add_test(NAME simple_continuous_time_system
#        COMMAND simple_continuous_time_system)
