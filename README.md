# 项目介绍
Kim Voice Assistant是基于阿里云服务的开源智能音箱，项目灵感来自jasper-client。

Kim在Jasper的基础上做了不少改进：

1. 基于Alibaba Cloud优秀的云端服务构建
1. 通过Docker管理运行环境，支持快速部署
1. 优化中文语义仲裁算法，更加精准的理解中文语义
2. 增加Web控制和OpenAPI的支持，提供丰富的设备的控制方式
2. 支持MQTT协议，对IoT设备提供控制方案

项目组成：

| 名称 | 描述 | 项目链接 |
|----|----|----|
| Kim Voice Assistant Dock | Kim服务运行Docker构建项目（设备端和服务端）  | [Dock](https://github.com/tenstone/kim-voice-assistant-dock) |
| Kim Voice Assistant Iot Client | Kim设备端项目 | [Client](https://github.com/tenstone/kim-voice-assistant-iot-client) |
| Kim Voice Assistant Server | Kim服务器端项目 | [Server](https://github.com/tenstone/kim-voice-assistant-server) |

# docker 镜像

https://hub.docker.com/r/mosch/raspberry-pi-snowboy/
https://hub.docker.com/r/resin/rpi-raspbian/'

# 构建

docker build -t kimserver kim-server/.



# 依赖
## Python依赖
二级依赖是需要在操作系统中安装的软件，如果你使用MacOS可以执行：
```
brew install xxx  
```
portaudio
##安装snowboy
编译安装ATLAS：
https://ncu.dl.sourceforge.net/project/math-atlas/Stable/3.10.3/atlas3.10.3.tar.bz2

```
pip3 install python-pyaudio python3-pyaudio sox
sudo apt-get install libatlas-base-dev
git clone https://github.com/swig/swig.git
pip install pyaudio
sudo apt-get install alsa-tools alsa-utils
sudo apt-get install libblas3 libblas-dev libatlas-dev libatlas-base-dev
sudo apt-get install python-cffi
sudo apt-get install libffi-dev
sudo apt-get install build-essential libssl-dev libffi-dev python3-dev
sudo apt-get install sox
sudo pip3 install RPi.GPIO
sudo pip3 install RPIO
```
如果出现错误，请参考：https://github.com/Kitt-AI/snowboy/issues/94
##安装rpi.gpio
```
sudo apt-get install python3-rpi.gpio
sudo systemctl enable pigpiod
```

| 依赖 | 描述 | 二级依赖 | 实现功能 |  
|-----|----|----|----|
| pyAudio | | 依赖portAudio | 音频播放 | 


