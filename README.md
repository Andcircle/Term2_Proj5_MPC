# Term2_Proj5_MPC
Use MPC to drive the vehicle on the track in simulation tool

The target of this project is: use MPC to drive the vehicle safely on the track in simulation tool using C++ (Eclipse IDE).

## Content of source code
- `src` source code directory:
  - `main.cpp` - communicate with simulation tool, call functions to solve MPC and update control parameter steering and acceleration.
  - `MPC.cpp` - feed MPC solver with initial state, constrants and simplified kinematic model, solve the MPC solver to get optimum control input. 

## MPC Model
![MPC](MPC.png)

Pls be noted:
Lidar can directly use standard Kalman filter, because the process function and measure function are both linear.
Radar has nonlinear measure function, which should be linearized use Jacobian matrix in each time step.

## Curve fitting

## MPC Parameter tuning

## Latency


## How to run the code
Clone this repo and perform
```
mkdir build && cd build
cmake ../src/  && make
./mpc
```




