add_executable (MembranePinch6
        main.cpp
        )


# if CMake cannot use find_package for Eigen, use the explicit include path instead
find_package(Eigen3)
# set(EIGEN3_INCLUDE_DIRS /usr/include/eigen3/)

find_package(PythonLibs)

#set(EIGEN3_INC_DIR /usr/local/include/eigen3) # Eigen header search path. (default). Change this if different in your system.


target_include_directories(MembranePinch6
        PUBLIC
            ${USD_INC_DIR}
            ${EIGEN3_INCLUDE_DIRS}
            ${PYTHON_INCLUDE_PATH}
        )

target_link_libraries(
        MembranePinch6
                ${USD_LIB_DIR}/libgf.dylib
                ${USD_LIB_DIR}/libsdf.dylib
                ${USD_LIB_DIR}/libtf.dylib
                ${USD_LIB_DIR}/libusd.dylib
                ${USD_LIB_DIR}/libusdGeom.dylib
                ${USD_LIB_DIR}/libvt.dylib
                ${USD_LIB_DIR}/libboost_python.dylib # todo find library
                ${PYTHON_LIBRARY}
        )
