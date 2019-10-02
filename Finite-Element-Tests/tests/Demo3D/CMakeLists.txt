add_executable (Demo3D
        main.cpp
        )


# if CMake cannot use find_package for Eigen, use the explicit include path instead
find_package(Eigen3)

find_package(PythonLibs)

#set(EIGEN3_INC_DIR /usr/local/include/eigen3) # Eigen header search path. (default). Change this if different in your system.

target_include_directories(Demo3D
        PUBLIC
            ${USD_INC_DIR}
            ${EIGEN3_INCLUDE_DIRS}
            ${PYTHON_INCLUDE_PATH}
        )

target_link_libraries(
        Demo3D
                ${USD_LIB_DIR}/libgf.dylib
                ${USD_LIB_DIR}/libsdf.dylib
                ${USD_LIB_DIR}/libtf.dylib
                ${USD_LIB_DIR}/libusd.dylib
                ${USD_LIB_DIR}/libusdGeom.dylib
                ${USD_LIB_DIR}/libvt.dylib
                ${USD_LIB_DIR}/libboost_python.dylib # todo find library
                ${PYTHON_LIBRARY}
        )
