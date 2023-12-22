# 单线雷达

**新增的功能**

```
1、修改雷达发布频率
2、调整雷达滤波

```

**功能测试**

```
启动单线雷达：
$ roslaunch livox_ros_driver livox_lidar_rviz_with_1_lidar.launch
```


**修改雷达的发布频率**

```
启动完成雷达节点之后:
$ rosrun rqt_reconfigure reconfigure

雷达的原始发布频率是28hz左右，在rqt_reconfigure中的skip修改为1，为14hz的发布频率。如果修改为0，为28hz的频率
```

**雷达滤波**

```
如果需要滤调雷达的一些激光数据，启动：
$ roslaunch laser_filters shadow_filter_example.launch 

通过修改laser_filters/examples/shadow_filter_example.yaml中的neighbors值的大小来调整所需滤波的大小

```
