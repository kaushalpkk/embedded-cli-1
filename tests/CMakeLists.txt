add_executable(embedded_cli_tests catch2/catch.cpp)

target_include_directories(embedded_cli_tests PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
        ${CMAKE_CURRENT_SOURCE_DIR}/catch2
        )

target_sources(embedded_cli_tests PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}/EmbeddedCliTest.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/EmbeddedCliTokensTest.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/CliMock.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/CliTestRunner.cpp
        )

target_link_libraries(embedded_cli_tests PRIVATE EmbeddedCLI::EmbeddedCLI)
