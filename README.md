# Raspberrypi4  
## Install tensorflow 2.1(2.2)  
tensorflow needs to be installed in 'sudo' mode in Raspberry Pi!!  
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

## Install opencv  
