# cmake_package_example
CMake package example (header only)

# Instructions:
1. "Compile" and install mylib:

        mkdir build
        cd build
        cmake .. -DCMAKE_INSTALL_PREFIX=/path/to/install_here
        cmake -build . -t install
2. Compile example app using mylib:

        cd usage_example
        mkdir build
        cd build
        cmake .. -DCMAKE_PREFIX_PATH=$(readlink -f /path/to/install_here/lib/cmake)
        cmake -build .
3. Run example app:

        cd usage_example/build
        ./example
