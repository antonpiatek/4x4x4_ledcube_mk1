set(CMAKE_TOOLCHAIN_FILE cmake/cmake/ArduinoToolchain.cmake) # Arduino Toolchain


cmake_minimum_required(VERSION 2.8)
project(cube C CXX)

set(ARDUINO_DEFAULT_BOARD uno) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyUSB0) # Default Port, when not specified
set(ARDUINO_DEFAULT_PROGRAMMER avrisp) # Default programmer, when not specified

print_board_list()
print_programmer_list()

generate_arduino_firmware(cube
    SKETCH cube
    )
