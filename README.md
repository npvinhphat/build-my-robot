# Build my world

This is the first project for Udacity's [Robotics Software Engineer Nanodegree Program](https://www.udacity.com/course/robotics-software-engineer--nd209), namely *Build My World*.

## How it works

This project just simply demonstrates how [Gazebo](http://gazebosim.org/) works, and how to write a plugin inside Gazebo. Upon launching the project, there should be a printed line in the terminal, indicating that the plugin works:

```
Welcome to Phat World!
```

## Usage

Make sure that you have installed Gazebo correctly, check [here](http://gazebosim.org/tutorials?cat=install) for the detailed installation.

First, choose your intended workspace directory and export the environment variable:

```
export PATH_TO_WORKSPACE = <your-path-to-intended-workspace>
```

Then, execute the following commands to pull the workspace and build the plugin code:

```
cd $PATH_TO_WORK_SPACE
git clone git@github.com:npvinhphat/build-my-robot.git
mkdir -p build-my-robot/build
cd build-my-robot/build
cmake ../
make
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:$PATH_TO_WORKSPACE/build-my-robot/build
```

Finally, run your gazebo world:

```
cd $PATH_TO_WORKSPACE/build-my-robot/world/
gazebo world
```

There should be a printed line `Welcome to Phat World!` indicating the plugin works, and the Gazebo world looks like below:

![alt image](https://user-images.githubusercontent.com/10416670/81493042-ecff4e00-92d7-11ea-94b1-176c3f9ae623.png)
