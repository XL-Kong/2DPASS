# 2DPASS

This is to detect foggy images and point clouds based on 2DPASS. The basic installation of the runtime environment can be referred to in OFFICIALREADME. The added content is mainly the depth complement of the point cloud and the fogging of the data.


## Fogify tools


### Depth completion
You can run the depth completion with
```shell script
cd <root dir of fogify_util>
python depth_completion.py --rgb the root of rgb image path --d the root of original depth image path --a the root of output path
```

### Image fogification
You can run the depth completion with
```shell script
cd <root dir of fogify_util>
python .\image_foggy --root path to root folder --beta 0.00016 
```

### Lidar fogification
You can run the depth completion with
```shell script
cd <root dir of fogify_util>
python .\Lidar_foggy --root path to root folder --beta 0.005 --sensor_type VelodyneHDLS3D
```
