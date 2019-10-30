# SLAM with Kinect Xbox-360 and RTAB-Map

## Installation of RTAB map
```
$ sudo apt-get update
$ sudo apt-get install libsqlite3-dev libpcl-dev libopencv-dev git cmake libproj-dev libqt5svg5-dev libsuitesparse-dev
```

Installing g2o
```
$ git clone https://github.com/RainerKuemmerle/g2o.git 
$ cd g2o
$ mkdir build
$ cd build
$ cmake -DBUILD_WITH_MARCH_NATIVE=OFF -DG2O_BUILD_APPS=OFF -DG2O_BUILD_EXAMPLES=OFF -DG2O_USE_OPENGL=OFF ..
$ make -j4
$ sudo make install
```

Installing GTSAM
```
$ git clone --branch 4.0.0-alpha2 https://github.com/borglab/gtsam.git gtsam-4.0.0-alpha2
$ cd gtsam-4.0.0-alpha2
$ mkdir build
$ cd build
$ cmake -DGTSAM_USE_SYSTEM_EIGEN=ON -DGTSAM_BUILD_EXAMPLES_ALWAYS=OFF -DGTSAM_BUILD_TESTS=OFF -DGTSAM_BUILD_UNSTABLE=OFF ..
$ make -j4
$ sudo make install
```
Installing RTAB-Map
```
$ git clone https://github.com/introlab/rtabmap.git rtabmap
$ cd rtabmap/build
$ cmake ..
$ make -j4
$ sudo make install
```
