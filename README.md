# **Discrete element method for self-compacted conrete mixer**
![GitHub - License](https://img.shields.io/badge/License-MIT-blue.svg)

More information is coming soon.


## __Requirements__
---
* Ubuntu 22.04
* ParaView 5.11.0

## __Package Version__
---
* LIGGGHTS-PUBLIC 3.8

## __Installation__
---
```bash
sudo apt-get install git
git clone https://github.com/CFDEMproject/LIGGGHTS-PUBLIC.git

```
Install packages
```bash
sudo apt-get install ffmpeg 
sudo apt install openmpi-bin
sudo snap install vlc 

sudo apt install cmake libavcodec-dev libavformat-dev libavutil-dev libboost-dev libdouble-conversion-dev libeigen3-dev libexpat1-dev libfontconfig-dev libfreetype6-dev libgdal-dev libglew-dev libhdf5-dev libjpeg-dev libjsoncpp-dev liblz4-dev liblzma-dev libnetcdf-dev libnetcdf-cxx-legacy-dev libogg-dev libpng-dev libpython3-dev libqt5opengl5-dev libqt5x11extras5-dev libsqlite3-dev libswscale-dev libtheora-dev libtiff-dev libxml2-dev libxt-dev qtbase5-dev qttools5-dev zlib1g-dev

sudo apt-get install -y paraview
```

CMake
```bash

cd ~/LIGGGHTS-PUBLIC/src
make auto

gedit MAKE/Makefile.user
USE_VTK is set to “ON”
AUTOINSTALL_VTK = "ON"

make auto
sudo rm /~/LIGGGHTS-PUBLIC/src/lmp_auto /bin/lmp380
sudo ln -s ~/LIGGGHTS-PUBLIC/src/lmp_auto /bin/lmp380
lmp380
```
Source the path
```bash
sudo gedit ~/../../etc/bash.bashrc
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:~/LIGGGHTS-PUBLIC/lib/vtk/install/lib/
lmp380
```

Run
```bash
mpirun -np {number of core} lmp380 -in {FILENAME}
paraview
```
---


