
## Requirements

- Protobuf 3.5+  进行编译，在CMakeLists.txt指定libprotobuf.a所在的路径
- OpenCV 4.0 With DNN module enabled  下载后完成编译。在CMakeLists.txt指定OpenCV_DIR
- Download ssd models. ( Google search   res10_300x300_ssd_iter_140000.caffemodel  deploy.prototxt.txt)
- Webcam (需要有摄像头支持)  


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

The following applications are generated.编译出以下的可执行文件

```
./ssd_face_detection
```

Parameters accepted from executables:
加上model和 proto进行在线人脸检测

```
cd data
cp res10_300x300_ssd_iter_140000.caffemodel deploy.prototxt.txt ../build
de build
 ./ssd_face_detection --model=./res10_300x300_ssd_iter_140000.caffemodel --proto=./deploy.prototxt.txt
```




 error while loading shared libraries: libopencv_imgcodecs.so.4.5: cannot open shared object file: No such file or directory
 ```
export LD_LIBRARY_PATH=opencv_path/lib

```