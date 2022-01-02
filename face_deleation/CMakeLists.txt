cmake_minimum_required (VERSION 3.0) 

PROJECT(face_detection)

set (CMAKE_CXX_STANDARD 11)


# Requires OpenCV v4.0 or later
set(OpenCV_DIR  ~/third_party/lib/cmake/opencv4)
FIND_PACKAGE( OpenCV 4 REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )

ADD_EXECUTABLE( image_detection image_detection.cpp )
TARGET_LINK_LIBRARIES( image_detection ${CONAN_LIBS} ${OpenCV_LIBS} /home/shuyongkang/third_party/source_code/protobuf-3.16.0/bazel-bin/libprotobuf.a)


ADD_EXECUTABLE( video_detection video_detection.cpp )
TARGET_LINK_LIBRARIES( video_detection  ${CONAN_LIBS} ${OpenCV_LIBS} /home/shuyongkang/third_party/source_code/protobuf-3.16.0/bazel-bin/libprotobuf.a)
