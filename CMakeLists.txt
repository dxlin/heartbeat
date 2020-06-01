cmake_minimum_required(VERSION 2.8)
project( HeartBeat )

#g++ -std=c++11 -I/usr/local/Cellar/opencv/4.0.1/include/opencv4 -lopencv_core -lopencv_dnn -lopencv_highgui -lopencv_imgcodecs -lopencv_imgproc -lopencv_objdetect -lopencv_video -lopencv_videoio Heartbeat.cpp opencv.cpp RPPG.cpp Baseline.cpp -o Heartbeat

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( HeartBeat Heartbeat.cpp opencv.cpp RPPG.cpp Baseline.cpp )
target_link_libraries( HeartBeat ${OpenCV_LIBS} )
