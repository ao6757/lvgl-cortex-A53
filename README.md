# LVGL

LVGL（Light and Versatile Graphics Library）是一个功能强大的嵌入式图形库，提供了丰富的绘图和用户界面功能。

本仓库是基于lv_drivers-release-v8.3、lvgl-release-v8.3、lv_port_linux_frame_buffer-master版本的定制版本。

## 特性

- 支持Cortex-A53开发板
- 其他lvgl相关特性和功能

## 屏幕触摸配置

如果您的屏幕触摸参数为1024x600，请按照以下步骤配置LVGL以适应您的屏幕和触摸：

1. 在LVGL的根目录下的lv_drv_conf.h中，到455行左右配置.
```
#define EVDEV_CALIBRATE 1

#if EVDEV_CALIBRATE
#define EVDEV_HOR_MIN 0
#define EVDEV_HOR_MAX 1024
#define EVDEV_VER_MIN 0
#define EVDEV_VER_MAX 600
#endif /EVDEV_CALIBRATE/
```

2. 根据新的屏幕和触摸参数，相应地调整您的应用程序界面和布局。

请注意，以上步骤只是指导，并且取决于您所使用的具体版本和配置。请参考LVGL的文档和示例以获取更详细的说明和指导。

## 安装和使用

在LVGL的根目录下make，然后把再生成的build/bin/目录下的demo文件复制到开发板上./deom运行。

## 贡献

如果您发现了bug或者有改进建议，请在GitHub上提出issue或者提交pull request。

## 许可证

LVGL遵循MIT许可证。请查看LICENSE文件以获取更多信息。