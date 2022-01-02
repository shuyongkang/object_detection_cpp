
## Requirements

- Protobuf 3.5
- OpenCV 4.0 With DNN module enabled
- Download YOLO v3 models. (Links provided on the book)
- Webcam (For face detection)


## Steps to build

To compile on Linux, mac or Windows using Mingw

```
mkdir build
cd build
cmake ..
make
```


#TODO  bazel build support
 
## Executables

The following applications are generated.

```
./video_detection  
./video_detection
```

Parameters accepted from executables:

```
./video_detection image_to_recognize_required
```

```
 ./video_detection --model=../data/res10_300x300_ssd_iter_140000.caffemodel --proto=../data/deploy.prototxt.txt
```



需要下载权重、config、coco.names   

TARGET_LINK_LIBRARIES( ${PROJECT_NAME}_face  ${CONAN_LIBS} ${OpenCV_LIBS} -lprotobuf)   学到了可以直接加-l
