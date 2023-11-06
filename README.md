# Ubuntu20.04 LSD-SLAM
## LSD-SLAM: Large-Scale Direct Monocular SLAM
## 1. Dependence
- QT5
```
	sudo apt-get install build-essential
	sudo apt-get install qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools
	sudo apt-get install qtcreator
	sudo apt-get install qt5*
```
	
- libQGLViewer-2.6.0
```
	git clone git@github.com:GillesDebunne/libQGLViewer.git
	cd libQGLViewer-2.6.0/QGLViewer
	qmake
	make
	sudo make install
```
- Opencv4.2

## 2. Build
```
	mkdir lsd_slam
	cd mkdir
	mkdir src
	cd src
	git clone git@github.com:huashu996/Ubuntu20.04LSD_SLAM.git
	cd ..
	catkin make
```
## 3. run
```
    另起终端
    roscore
    另起终端
    source devel/setup.bash	
    rosrun lsd_slam_viewer viewer
    另起终端
    source devel/setup.bash
    rosrun lsd_slam_core live_slam image:=/image_raw camera_info:=/camera_info
    另起终端   
    source devel/setup.bash 
    rosbag play LSD_room_pc.bag
```

