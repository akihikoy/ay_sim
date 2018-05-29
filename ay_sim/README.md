ay_sim
==================
Simulations with ODE (open dynamics engine) including pouring, a hopping robot, etc.

`ay_sim` is built on ROS, implemented with C++ using ODE.


Author
==================
Akihiko Yamaguchi, http://akihikoy.net/


Requirements
==================
See `manifest.xml`.

Need to build from source (**not ROS**):
- ODE (Open Dynamics Engine; a simulator)
  - http://ode.org/
  - We assume that the ODE is built in `$HOME/prg/libode/ode-latest/` from source.
  - Rename ODE directory from `ode-0.1X/` to `ode-latest/` or make a symbolic link.
  - Use `./configure --enable-double-precision --disable-asserts` to setup.
  - Build `drawstuff` as well (this is default).
  - Test demo (e.g. `ode-latest/ode/demo/demo_buggy`) to check the installation.


Directories
==================

include/ay_sim
----------------------------
ROS-independent header files (C++).

src
----------------------------
ROS-independent source files (C++).

src_ros
----------------------------
ROS-dependent source files (C++).  Mainly, programs of ROS nodes are contained.


Build
==================
The repository directory should be in ROS workspace (e.g. ~/ros_ws/).
Build `ay_sim` with `rosmake`.

```
$ rosmake ay_sim
```

After `rosmake`, you will find some executables in `bin/` directory.
There will be some directories made by `rosmake`.


Usage
==================

ode_grpour_sim
---------------------------
Pouring simulation.
Launch by:

```
$ roslaunch ay_sim ode_grpour_sim1.launch
```

Examples to control from Python over ROS, see ay_trick.

ode_hopper1
---------------------------
Hopping robot simulation.
Launch by:

```
$ roslaunch ay_sim ode_hopper1_1.launch
```

Examples to control from Python over ROS, see ay_trick.


Troubles
==================
Send e-mails to the author.
