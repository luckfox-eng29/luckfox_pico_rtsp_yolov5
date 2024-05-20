**Read this in other languages: [English](README.md), [中文](README_CN.md).**

# luck_pico_rtsp_yolov5
    Test luckfox-pico pro (128MB RAM) using rknn to infer retinaface and stream it via rtsp.

# Development Environment
+ [Luckfox-pico SDK(Only rootfs built by buildroot is supported)](https://github.com/LuckfoxTECH/luckfox-pico)

# Compilation
```
export LUCKFOX_SDK_PATH=<Your Luckfox-pico SDK Path>
mkdir build
cd build
cmake ..
make && make install
```

# Execution
Upload the compiled `luckfox_rtsp_yolov5_demo` (directory) to luckfox-pico, navigate to the directory, and run
```
./luckfox_rtsp_yolov5
```
Use VLC to open the network stream at rtsp://172.32.0.93/live/0 (modify the IP address according to your actual situation).

**Note**: Before running, please close the default rkipc program by executing `RkLunch-stop.sh`.
Due to the large size of the yolov5 model, it requires more memory resources to load and cannot run on luckfox-pico mini/plus (rv1103).

#  Related Tutorials
https://wiki.luckfox.com/Luckfox-Pico/RKMPI-example/
