
#### Python Setup
```
$ sudo apt install virtualenv

$ virtualenv -p python3.6 $HOME/venv
$ source $HOME/venv/bin/activate
```

#### セットアップ

```
$ pip3 install gym-ignition
```

#### gym ignitionの拡張

```
$ sudo apt install gcc-8 g++-8
$ export CC=gcc-8
$ export CXX=g++-8

$ sudo apt install swig

$ git clone https://github.com/robotology/gym-ignition.git
$ cd gym-ignition/
$ mkdir build/
$ cd build/
$ cmake -DCMAKE_INSTALL_PREFIX=/usr/local ..
$ cmake --build .
$ sudo cmake --build . --target install

$ cd ..
$ pip3 uninstall gym-ignition
$ pip3 install -e .

$ export PYTHONPATH=/usr/local/lib/python3.6/site-packages/
$ python3 ~/gym-ignition/examples/python/launch_cartpole.py

```