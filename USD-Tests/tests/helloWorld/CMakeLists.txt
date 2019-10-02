add_executable (helloWorld
        main.cpp
        )

target_include_directories(helloWorld
        PUBLIC
            ${USD_INC_DIR}
        )

target_link_libraries(
        helloWorld
<<<<<<< HEAD
                ${USD_LIB_DIR}/libgf.so
                ${USD_LIB_DIR}/libsdf.so
                ${USD_LIB_DIR}/libtf.so
                ${USD_LIB_DIR}/libusd.so
                ${USD_LIB_DIR}/libusdGeom.so
                ${USD_LIB_DIR}/libvt.so
=======
                ${USD_LIB_DIR}/libhd.dylib
                ${USD_LIB_DIR}/libhdSt.dylib
                ${USD_LIB_DIR}/libhdx.dylib
                ${USD_LIB_DIR}/libtf.dylib
                ${USD_LIB_DIR}/libusd.dylib
                ${USD_LIB_DIR}/libusdGeom.dylib
                ${USD_LIB_DIR}/libsdf.dylib
                ${USD_LIB_DIR}/libgarch.dylib
                ${USD_LIB_DIR}/libcameraUtil.dylib
                ${USD_LIB_DIR}/libgf.dylib
                ${USD_LIB_DIR}/libglf.dylib
                ${USD_LIB_DIR}/libvt.dylib
                ${USD_LIB_DIR}/libpxOsd.dylib
                ${USD_LIB_DIR}/libosdCPU.dylib
                ${USD_LIB_DIR}/libboost_python.dylib # todo find library
                ${PYTHON_LIBRARY}
                ${OPENGL_LIBRARIES}
>>>>>>> 4d8bd26... Make build changes for Mac
        )
