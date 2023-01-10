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
The dataset should be pre-prepared in KITTI or NuScenes format before it is processed. The data after fogification should be as shown below (in KITTI format).
```
./dataset/
├── 
├── ...
└── SemanticKitti/
    ├──sequences
        ├── 00/           
        │   ├── velodyne/	
        |   |	├── 000000.bin
        |   |	├── 000001.bin
        |   |	└── ...
        │   └── labels/ 
        |   |   ├── 000000.label
        |   |   ├── 000001.label
        |   |   └── ...
        |   └── image_2/ 
        |   |   ├── 000000.png
        |   |   ├── 000001.png
        |   |   └── ...
        |   calib.txt
        ├── 08/ # for validation
        ├── 11/ # 11-21 for testing
        └── 21/
	    └── ...
```
You can modify the corresponding file in config with different naming. It is worth mentioning that KITTI's 11-21 does not really need to be used here due to the large number of samples, but it is necessary to create a corresponding folder and store at least one sample.


## Foggy-KITTI dataset

The already processed dataset can be downloaded from [this Onedrive folder](https://nusu-my.sharepoint.com/:f:/r/personal/e1011066_u_nus_edu/Documents/KITTI?csf=1&web=1&e=8T5OUG)
