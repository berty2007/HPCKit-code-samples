set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS}")
add_executable (mandelbrot main.cpp syclObject.cpp mandelSerial.cpp)
target_link_libraries(mandelbrot OpenCL sycl)
add_custom_target (run ./mandelbrot)
