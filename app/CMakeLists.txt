add_avr_executable (
    two_wire_interface_avr
    main.cpp
)

find_library(C_LIB c)
message(STATUS "avr-libc: ${C_LIB}")

avr_target_link_libraries(two_wire_interface_avr mylib ${C_LIB})
