cmake_minimum_required(VERSION 3.0.0)
project(BarcodeMaker VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories(include/)
add_executable(BarcodeMaker src/main.c src/bit_string.c src/buffer.c src/qr_encode.c src/constant_tables.c src/unit_tests.c src/qr_polynomials.c src/qr_structure.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
