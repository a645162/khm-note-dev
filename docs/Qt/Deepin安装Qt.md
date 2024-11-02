# Deepin安装Qt6

测试环境`Deepin 23`

## Qt6

```bash
sudo apt install qtcreator
sudo apt install qt6-base-dev
# Or
sudo apt install qt6*
```

## OpenGL

```bash
# 注：安装系统时没有选择边安装边更新，此处会缺依赖库
sudo apt-get install build-essential
sudo apt-get install libgl1-mesa-dev
sudo apt-get install libglu1-mesa-dev
sudo apt-get install freeglut3-dev
```

## Ref

https://blog.csdn.net/qq_24489251/article/details/117981382
https://blog.csdn.net/qq_38880380/article/details/126492110
