# 2DPASS

This is to detect foggy images and point clouds based on 2DPASS. The basic installation of the runtime environment can be referred to in OFFICIALREADME. The added content is mainly the depth complement of the point cloud and the fogging of the data.


## Fogify tools


### depth completion
You can run the depth completion with
```shell script
cd <root dir of fogify_util>
python depth_completion.py --rgb the root of rgb image path --d the root of original depth image path --a the root of output path
```

### image fogification


### Lidar fogification
