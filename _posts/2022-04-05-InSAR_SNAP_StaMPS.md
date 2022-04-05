## SNAP_StaMPS

There are the steps of PS-InSAR using SNAP_StaMPS

### STEP1

The first step is to find a region of interest and download the Sentinel-1 images. We can use Google Earth Engine and PIE Engine to have a look at first.
Then we can use the ASF website <https://search.asf.alaska.edu/> to find and download the images.

### STEP2

We can use model folder in this STEP. Every step out put have been devided to a certain folder so it is clear.

#### 2.1 Split

Just use SNAP to split. This is because sentinel-1 image have 3 IW. Use this step to choose the IW that we want to use.

#### 2.2 Apply Orbit

This step is to apply the precious orbit files. Sometimes it can be downloaded automatically but most of the time we have to download it manually.
To download it manually we need a python script written by YK. First, the folder contains the zips should be changed. Second, the folder that you want to download orbit file to should be changed. Third, because of the cookie, the 'asf-urs' need to be changed.

#### 2.1 + 2.2

### 2.3 Registration

Yes, this step is just registration. However, it's better to put the images in order and use the 1s DEM. 
This step will last for a relatively long time.

### 2.4 Deburst

It's just deburst. Just because Sentinel-1 images have the burst.

### 2.5 Merge

Sometimes merge is required when the Region Of Interest belongs to more than one IW.

### 2.6
