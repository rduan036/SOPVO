#  sopvo
## 

### 1-Demo Video
EuRoC benchmark test:
[![](http://img.youtube.com/vi/5MypXkwQwFk/0.jpg)](http://www.youtube.com/watch?v=5MypXkwQwFk "SOPVO EuRoC benchmark test")

T265+drone on board test:
[![](http://img.youtube.com/vi/Yr2lf6Kxt3U/0.jpg)](http://www.youtube.com/watch?v=Yr2lf6Kxt3U "SOPVO T265+drone on board test")

### 2-Relevent Publication:
TBD
### 3-Support Camera/Dataset:
EuRoC MAV Dataset, Intel Realsense T265, KITTI(ros melodic)
### 4-Build The Project
We have tested in the following environment: <br />
Ubuntu 16.04 + ROS Kinetic (recommend) <br />
Ubuntu 18.04 + ROS melodic (parameters in config file need to be refined) <br />

4.1 Clone the repository to the catkin work space eg. /catkin_ws/src

4.2 Install sopvo:
````
./install_sopvo_XXXX.sh
````
4.3 Compile
````
cd ~/catkin_ws
catkin_make
````
### 5-Verification
5.1 EuRoC MAV Dataset
Download the dataset(say MH_05_difficult) into the bag folder:
````
roscd sopvo/bag/
wget http://robotics.ethz.ch/~asl-datasets/ijrr_euroc_mav_dataset/machine_hall/MH_05_difficult/MH_05_difficult.bag
````
Edit the corresponding bag name in sopvo_euroc.launch file:
````
<node pkg="rosbag" type="play" name="rosbag" args="$(find sopvo)/bag/MH_05_difficult.bag"/>
````
run the following launch files:
````
roslaunch sopvo sopvo_euroc.launch
````

5.2 Intel Realsense T265 (live version):
make sure you have installed realsense-ros properly.
````
roslaunch sopvo sopvo_t265_live.launch
````

5.3 KITTI:
please download the odometry dataset(gray image), then use kitti_img2rosbag_tool to convert the sequense into rosbag.
There are different image resolutions of the KITTI datasets, please modify the config files for the testing. 
In folder ./config we provide two example: kitti_1226.yaml and kitti_1241.yaml. 

5.4 Other datasets:
please wait for update

### Maintainer:
Ran Duan, ArcLab at PolyU, HK, China
ran-sn.duan@connect.polyu.hk
rduan036@gmail.com
