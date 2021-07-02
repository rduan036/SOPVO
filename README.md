### PS: This is a UAV onboard version, for testing off-line, kindly check our main project here: 
https://github.com/arclab-hku/SOPVO

### Install (kinetic or melodic)
````
./install_sopvo_XXXX.sh

cd YOUR_WORK_SPACE

catkin_make
````

### Run demo (D435i)
UAV platform: lattepanda + D435i. Please install realsense-ros first.

````
roslaunch sopvo sopvo_d435i.launch

roslaunch sopvo px4.launch
````

You should see the results below:
<img src="results/rviz.png" width="600"> <br />
<img src="results/sopvo_onboard.gif" width="600"> <br />
<img src="results/qt_graph.png" width="600"> <br />

PS: please tuning your PX4 para, espectially EKF for pose fusion.

### Maintainer:

Ran Duan, ArcLab at PolyU, HK, China
ran-sn.duan@connect.polyu.hk
rduan036@gmail.com
