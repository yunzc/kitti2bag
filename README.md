# kitti2bag

[![Build Status](https://travis-ci.org/tomas789/kitti2bag.svg?branch=master)](https://travis-ci.org/tomas789/kitti2bag)

Convert [KITTI](http://www.cvlibs.net/datasets/kitti/index.php) dataset to ROS bag file the easy way!

![KITTI playback preview](https://raw.githubusercontent.com/tomas789/kitti2bag/gh-pages/img/kitti_playback.png)

## NOTE 
This only works with [my version of pykitti](https://github.com/yunzc/pykitti). 
Download this (make sure you remove any other installed pykitti) and in the pykitti repository, run 
```
python setup.py develop
```

## Acknowledgements 

Many thanks to the [original repository](https://github.com/tomas789/kitti2bag/pulls) this one is forked off from.

## Setup

In the repository, run 
```
python setup.py develop
```

## How to run it?

Download a kitti dataset to some folder of your choosing. For example, the synced data for `2011_09_26_drive_0002`. In this folder, do: 
```bash
$ kitti2bag -t 2011_09_26 -r 0002 raw_synced
```
and the result should be saved as `kitti_2011_09_26_drive_0002_synced.bag`

Or you could download the unsynced data for `2011_09_26_drive_0002`. Then you can do: 
```bash
$ kitti2bag -t 2011_09_26 -r 0002 raw_unsynced
```
and the result should be saved as `kitti_2011_09_26_drive_0002_unsynced.bag`

```bash
## OVERVIEW ##
path:        kitti_2011_09_26_drive_0002_synced.bag
version:     2.0
duration:    7.8s
start:       Sep 26 2011 13:02:44.33 (1317042164.33)
end:         Sep 26 2011 13:02:52.16 (1317042172.16)
size:        417.2 MB
messages:    1078
compression: none [308/308 chunks]
types:       geometry_msgs/TwistStamped [98d34b0043a2093cf9d9345ab6eef12e]
             sensor_msgs/CameraInfo     [c9a58c1b0b154e0e6da7578cb991d214]
             sensor_msgs/Image          [060021388200f6f0f447d0fcd9c64743]
             sensor_msgs/Imu            [6a62c6daae103f4ff57a132d6f95cec2]
             sensor_msgs/NavSatFix      [2d3a8cd499b9b4a0249fb98fd05cfa48]
             sensor_msgs/PointCloud2    [1158d486dd51d683ce2f1be655c3c181]
             tf2_msgs/TFMessage         [94810edda583a504dfda3829e70d7eec]
topics:      /kitti/camera_color_left/camera_info    77 msgs    : sensor_msgs/CameraInfo    
             /kitti/camera_color_left/image_raw      77 msgs    : sensor_msgs/Image         
             /kitti/camera_color_right/camera_info   77 msgs    : sensor_msgs/CameraInfo    
             /kitti/camera_color_right/image_raw     77 msgs    : sensor_msgs/Image         
             /kitti/camera_gray_left/camera_info     77 msgs    : sensor_msgs/CameraInfo    
             /kitti/camera_gray_left/image_raw       77 msgs    : sensor_msgs/Image         
             /kitti/camera_gray_right/camera_info    77 msgs    : sensor_msgs/CameraInfo    
             /kitti/camera_gray_right/image_raw      77 msgs    : sensor_msgs/Image         
             /kitti/oxts/gps/fix                     77 msgs    : sensor_msgs/NavSatFix     
             /kitti/oxts/gps/vel                     77 msgs    : geometry_msgs/TwistStamped
             /kitti/oxts/imu                         77 msgs    : sensor_msgs/Imu           
             /kitti/velo/pointcloud                  77 msgs    : sensor_msgs/PointCloud2   
             /tf                                     77 msgs    : tf2_msgs/TFMessage        
             /tf_static                              77 msgs    : tf2_msgs/TFMessage
```