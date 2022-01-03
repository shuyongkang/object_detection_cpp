
## Requirements

- Protobuf 3.5+
- OpenCV 4.0 With DNN module enabled
- Download YOLO v3 models(.cfg and .weights). ([Links provided on the book](https://pjreddie.com/darknet/yolo/))
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
./yolov3_image_detection  
```

Parameters accepted from executables:

```
cd data
cp coco.names test.jpeg yolov3-tiny.cfg yolov3-tiny.weights ../build/
./yolov3_image_detection image_to_recognize_required
```

