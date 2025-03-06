option(ENABLE_TEST "Enable Unit Tests" OFF)
if(ENABLE_TEST AND NOT STORMBYTE_AS_DEPENDENCY)
	enable_testing()

	add_executable(LoggerTests logger_test.cxx)
	target_link_libraries(LoggerTests StormByte::Logger)
	add_test(NAME LoggerTests COMMAND LoggerTests)
endif()