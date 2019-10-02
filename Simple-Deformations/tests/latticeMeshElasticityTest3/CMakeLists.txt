add_executable (latticeMeshElasticityTest3
        main.cpp
        )

find_package(PythonLibs)

set(EIGEN3_INC_DIR /usr/local/include/eigen3) #changing the include path for Eigen. In my system, I have installed it at /usr/local/include directory (the default). Change the path if your directory does not match this path. 

target_include_directories(latticeMeshElasticityTest3
        PUBLIC
            ${USD_INC_DIR}
            ${EIGEN3_INC_DIR}
            ${PYTHON_INCLUDE_PATH}
        )

target_link_libraries(
        latticeMeshElasticityTest3
                ${USD_LIB_DIR}/libgf.dylib
                ${USD_LIB_DIR}/libsdf.dylib
                ${USD_LIB_DIR}/libtf.dylib
                ${USD_LIB_DIR}/libusd.dylib
                ${USD_LIB_DIR}/libusdGeom.dylib
                ${USD_LIB_DIR}/libvt.dylib
                ${USD_LIB_DIR}/libboost_python.dylib # todo find library
                ${PYTHON_LIBRARY}
        )
