
## Requirements
- Protobuf 3.5+  进行编译，在CMakeLists.txt指定libprotobuf.a所在的路径
- OpenCV 4.0 With DNN module enabled  下载后完成编译。在CMakeLists.txt指定OpenCV_DIR
- Download YOLO v3 models(.cfg and .weights).下载到data目录中， ([Links ](https://pjreddie.com/darknet/yolo/))
代码中使用的是yolov3-tiny.weights和yolov3-tiny.cfg，如果是yolov3,需要修改代码。

## Steps to build

To compile on Linux, 完成 编译
```
mkdir build
cd build
cmake ..
make
```


 
## Executables  执行

The following applications are generated. 编译后会生成以下文件

```
./yolov3_image_detection  
```

Parameters accepted from executables:

```
cd data
cp coco.names test.jpeg yolov3-tiny.cfg yolov3-tiny.weights ../build/
./yolov3_image_detection test.jpg
```

完成检测后会将结果保存在result.jpg中

#TODO  bazel build support