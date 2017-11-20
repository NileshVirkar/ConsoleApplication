CMAKE_MINIMUM_REQUIRED(VERSION 3.1.0)

SET(RUNNER_EXE_NAME consoleApplication)
ADD_EXECUTABLE(${RUNNER_EXE_NAME} "")
set(CMAKE_CXX_STANDARD 14)
set(BOOST_ROOT "" CACHE PATH "")
if (BOOST_ROOT STREQUAL "") 
message(FATAL_ERROR ":Required Boost source directory path")
endif () 

INCLUDE_DIRECTORIES(${BOOST_ROOT})

target_sources(${RUNNER_EXE_NAME}
    PRIVATE
	${CMAKE_SOURCE_DIR}/ConsoleApplication/src/Another.cpp
	${CMAKE_SOURCE_DIR}/ConsoleApplication/src/ConsoleApplication.cpp
	${CMAKE_SOURCE_DIR}/ConsoleApplication/src/ConsoleApplication.cpp
)



