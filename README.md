# Raspberrypi4  
## Install tensorflow 2.1(2.2)  
tensorflow needs to be installed in 'sudo' mode in Raspberry Pi 4  
It can not use 'pip3 install tensorflow', and will get the 'version 1.14'(can't upgrade) even latest pip version.  
```bash
# get a fresh start
$ sudo apt-get update
$ sudo apt-get upgrade
# remove old versions, if not placed in a virtual environment (let pip search for them)
$ sudo pip uninstall tensorflow
$ sudo pip3 uninstall tensorflow
# install the dependencies (if not already onboard)
$ sudo apt-get install gfortran
$ sudo apt-get install libhdf5-dev libc-ares-dev libeigen3-dev
$ sudo apt-get install libatlas-base-dev libopenblas-dev libblas-dev
$ sudo apt-get install liblapack-dev cython
$ sudo pip3 install pybind11
$ sudo pip3 install h5py
# download the wheel
$ wget https://github.com/Qengineering/Tensorflow-Raspberry-Pi/raw/master/tensorflow-2.1.0-cp37-cp37m-linux_armv7l.whl
# install TensorFlow
$ sudo -H pip3 install tensorflow-2.1.0-cp37-cp37m-linux_armv7l.whl
# and complete the installation by rebooting
$ reboot
```
Reference:  
tf 2.1 https://qengineering.eu/install-tensorflow-2.1.0-on-raspberry-pi-4.html  
tf 2.2 https://qengineering.eu/install-tensorflow-2.2.0-on-raspberry-pi-4.html  
  
## Install opencv  
The latest version of openCV will get the problem on Raspberry Pi.  
```
cv2.error: OpenCV(4.4.0) /tmp/pip-install-rrmos8ri/opencv-python/opencv/modules/highgui/src/window.cpp:651: error: (-2:Unspecified error) The function is not implemented. Rebuild the library with Windows, GTK+ 2.x or Cocoa support. If you are on Ubuntu or Debian, install libgtk2.0-dev and pkg-config, then re-run cmake or configure script in function 'cvShowImage'
```  
I got the right version with these two packages.  
```bash
pip3 install opencv-python==4.1.1.26
pip3 install opencv-contrib-python==4.1.0.25
```


