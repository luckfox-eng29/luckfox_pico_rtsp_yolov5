**其他语言版本: [English](README.md), [中文](README_CN.md).**

# luck_pico_rtsp_yolov5
    测试 luckfox-pico pro (128MB RAM) 使用 rknn 推理 retinaface 并进行 rtsp 推流。

# 开发环境
+ luckfox-pico sdk

# 编译
```
export LUCKFOX_SDK_PATH=<Your Luckfox-pico Sdk Path>
mkdir build
cd build
cmake ..
make && make install
```

# 运行
将编译生成的`luckfox_rtsp_yolov5_demo`上传到 luckfox-pico 上，进入文件夹运行
```
./luckfox_rtsp_yolov5
```
使用 vlc 打开网络串流 rtsp://172.32.0.93/live/0（按实际情况修改IP地址拉取图像）

**注意**：运行前请关闭系统默认 rkipc 程序，执行 `RkLunch-stop.sh` 关闭。
由于 yolov5 模型较大需要消耗更多的内存资源加载，在 luckfox-pico mini/plus （rv1103）上无法运行。


