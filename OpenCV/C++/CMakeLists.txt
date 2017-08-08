cmake_minimum_required( VERSION 2.6 )
set(CMAKE_CXX_COMPILER /usr/bin/g++)
find_package( OpenCV REQUIRED )

project( Calib )
add_executable( Calib src/calibration.cpp )
target_link_libraries( Calib ${OpenCV_LIBS} )

project( StereoCalib )
add_executable( StereoCalib src/stereocalibrate.cpp )
target_link_libraries( StereoCalib ${OpenCV_LIBS} )
