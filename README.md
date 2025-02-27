# Machine Learning Containers for Jetson and JetPack

Hosted on [NVIDIA GPU Cloud](https://ngc.nvidia.com/catalog/containers?orderBy=modifiedDESC&query=L4T&quickFilter=containers&filters=) (NGC) are the following Docker container images for machine learning on Jetson:

* [`l4t-ml`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-ml)
* [`l4t-pytorch`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-pytorch)
* [`l4t-tensorflow`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-tensorflow)

The following ROS containers are also provided, which can be pulled from DockerHub or built for JetPack 4.4 or newer:

* ROS Melodic (`ros:melodic-ros-base-l4t-r32.5.0`)
* ROS Noetic (`ros:noetic-ros-base-l4t-r32.5.0`)
* ROS2 Eloquent (`ros:eloquent-ros-base-l4t-r32.5.0`)
* ROS2 Foxy (`ros:foxy-ros-base-l4t-r32.5.0`)
* ROS2 Galactic (`ros:galactic-ros-base-l4t-r32.5.0`)

## Pre-built Container Images

The following images can be pulled from NGC or DockerHub without needing to build the containers yourself:

|                                                                                     | L4T Version | Container Tag                                      |
|-------------------------------------------------------------------------------------|:-----------:|----------------------------------------------------|
| [`l4t-ml`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-ml)                 |   R32.5.0*  | `nvcr.io/nvidia/l4t-ml:r32.5.0-py3`                |
|                                                                                     |   R32.4.4   | `nvcr.io/nvidia/l4t-ml:r32.4.4-py3`                |
|                                                                                     |   R32.4.3   | `nvcr.io/nvidia/l4t-ml:r32.4.3-py3`                |
| [`l4t-pytorch`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-pytorch)       |   R32.5.0*  | `nvcr.io/nvidia/l4t-pytorch:r32.5.0-pth1.7-py3`    |
|                                                                                     |   R32.5.0*  | `nvcr.io/nvidia/l4t-pytorch:r32.5.0-pth1.6-py3`    |
|                                                                                     |   R32.4.4   | `nvcr.io/nvidia/l4t-pytorch:r32.4.4-pth1.6-py3`    |
|                                                                                     |   R32.4.3   | `nvcr.io/nvidia/l4t-pytorch:r32.4.3-pth1.6-py3`    |
| [`l4t-tensorflow`](https://ngc.nvidia.com/catalog/containers/nvidia:l4t-tensorflow) |   R32.5.0*  | `nvcr.io/nvidia/l4t-tensorflow:r32.5.0-tf1.15-py3` |
|                                                                                     |   R32.5.0*  | `nvcr.io/nvidia/l4t-tensorflow:r32.5.0-tf2.3-py3`  |
|                                                                                     |   R32.4.4   | `nvcr.io/nvidia/l4t-tensorflow:r32.4.4-tf1.15-py3` |
|                                                                                     |   R32.4.4   | `nvcr.io/nvidia/l4t-tensorflow:r32.4.4-tf2.3-py3`  |
|                                                                                     |   R32.4.3   | `nvcr.io/nvidia/l4t-tensorflow:r32.4.3-tf1.15-py3` |
|                                                                                     |   R32.4.3   | `nvcr.io/nvidia/l4t-tensorflow:r32.4.3-tf2.2-py3`  |
| [`ROS Melodic`](https://hub.docker.com/repository/docker/dustynv/ros)               |   R32.6.1   | `dustynv/ros:melodic-ros-base-l4t-r32.6.1`         |
|                                                                                     |   R32.5.0*  | `dustynv/ros:melodic-ros-base-l4t-r32.5.0`         |
|                                                                                     |   R32.4.4   | `dustynv/ros:melodic-ros-base-l4t-r32.4.4`         |
| [`ROS Noetic`](https://hub.docker.com/repository/docker/dustynv/ros)                |   R32.6.1   | `dustynv/ros:noetic-ros-base-l4t-r32.6.1`          |
|                                                                                     |   R32.5.0*  | `dustynv/ros:noetic-ros-base-l4t-r32.5.0`          |
|                                                                                     |   R32.4.4   | `dustynv/ros:noetic-ros-base-l4t-r32.4.4`          |
| [`ROS2 Eloquent`](https://hub.docker.com/repository/docker/dustynv/ros)             |   R32.6.1   | `dustynv/ros:eloquent-ros-base-l4t-r32.6.1`        |
|                                                                                     |   R32.5.0*  | `dustynv/ros:eloquent-ros-base-l4t-r32.5.0`        |
|                                                                                     |   R32.4.4   | `dustynv/ros:eloquent-ros-base-l4t-r32.4.4`        |
| [`ROS2 Foxy`](https://hub.docker.com/repository/docker/dustynv/ros)                 |   R32.6.1   | `dustynv/ros:foxy-ros-base-l4t-r32.6.1`            |
|                                                                                     |   R32.5.0*  | `dustynv/ros:foxy-ros-base-l4t-r32.5.0`            |
|                                                                                     |   R32.4.4   | `dustynv/ros:foxy-ros-base-l4t-r32.4.4`            |
| [`ROS2 Galactic`](https://hub.docker.com/repository/docker/dustynv/ros)             |   R32.6.1   | `dustynv/ros:galactic-ros-base-l4t-r32.6.1`        |
|                                                                                     |   R32.5.0*  | `dustynv/ros:galactic-ros-base-l4t-r32.5.0`        |
|                                                                                     |   R32.4.4   | `dustynv/ros:galactic-ros-base-l4t-r32.4.4`        |

> **note:** the L4T R32.5.0 containers can be run on both JetPack 4.5 (L4T R32.5.0) and JetPack 4.5.1 (L4T R32.5.1)

To download and run one of these images, you can use the included run script from the repo:

``` bash
$ scripts/docker_run.sh -c nvcr.io/nvidia/l4t-pytorch:r32.5.0-pth1.7-py3
```

For other configurations, below are the instructions to build and test the containers using the included Dockerfiles.

## Docker Default Runtime

To enable access to the CUDA compiler (nvcc) during `docker build` operations, add `"default-runtime": "nvidia"` to your `/etc/docker/daemon.json` configuration file before attempting to build the containers:

``` json
{
    "runtimes": {
        "nvidia": {
            "path": "nvidia-container-runtime",
            "runtimeArgs": []
        }
    },

    "default-runtime": "nvidia"
}
```

You will then want to restart the Docker service or reboot your system before proceeding.

## Building the Containers

To rebuild the containers from a Jetson device running [JetPack 4.4](https://developer.nvidia.com/embedded/jetpack) or newer, first clone this repo:

``` bash
$ git clone https://github.com/dusty-nv/jetson-containers
$ cd jetson-containers
```

Before proceeding, make sure you have set your [Docker Default Runtime](#docker-default-runtime) to `nvidia` as shown above.

### ML Containers

To build the ML containers (`l4t-pytorch`, `l4t-tensorflow`, `l4t-ml`), use [`scripts/docker_build_ml.sh`](scripts/docker_build_ml.sh) - along with an optional argument of which container(s) to build: 

``` bash
$ ./scripts/docker_build_ml.sh all        # build all: l4t-pytorch, l4t-tensorflow, and l4t-ml
$ ./scripts/docker_build_ml.sh pytorch    # build only l4t-pytorch
$ ./scripts/docker_build_ml.sh tensorflow # build only l4t-tensorflow
```

> You have to build `l4t-pytorch` and `l4t-tensorflow` to build `l4t-ml`, because it uses those base containers in the multi-stage build.

Note that the TensorFlow and PyTorch pip wheel installers for aarch64 are automatically downloaded in the Dockerfiles from the [Jetson Zoo](https://elinux.org/Jetson_Zoo).

### ROS Containers

To build the ROS containers, use [`scripts/docker_build_ros.sh`](scripts/docker_build_ros.sh) with the `--distro` option to specify the name of the ROS distro to build:

``` bash
$ ./scripts/docker_build_ros.sh --distro all       # build all of the below (default)
$ ./scripts/docker_build_ros.sh --distro melodic   # build only melodic
$ ./scripts/docker_build_ros.sh --distro noetic    # build only noetic
$ ./scripts/docker_build_ros.sh --distro eloquent  # build only eloquent
$ ./scripts/docker_build_ros.sh --distro foxy      # build only foxy
$ ./scripts/docker_build_ros.sh --distro galactic  # build only galactic
```

You can also specify `--with-pytorch` and `--with-slam` to build variants with support for PyTorch and GPU-accelerated SLAM nodes (including ORBSLAM2 and RTABMAP).  Note that Noetic, Foxy, and Galactic are built from source for Ubuntu 18.04, while Melodic and Eloquent are installed from Debian packages into the containers.

## Testing the Containers

To run a series of automated tests on the packages installed in the containers, run the following from your `jetson-containers` directory:

``` bash
$ ./scripts/docker_test_ml.sh all        # test all: l4t-pytorch, l4t-tensorflow, and l4t-ml
$ ./scripts/docker_test_ml.sh pytorch    # test only l4t-pytorch
$ ./scripts/docker_test_ml.sh tensorflow # test only l4t-tensorflow
```

To test ROS:

``` bash
$ ./scripts/docker_test_ros.sh all       # test if the build of ROS all was successful: 'melodic', 'noetic', 'eloquent', 'foxy'
$ ./scripts/docker_test_ros.sh melodic   # test if the build of 'ROS melodic' was successful
$ ./scripts/docker_test_ros.sh noetic    # test if the build of 'ROS noetic' was successful
$ ./scripts/docker_test_ros.sh eloquent  # test if the build of 'ROS eloquent' was successful
$ ./scripts/docker_test_ros.sh foxy      # test if the build of 'ROS foxy' was successful
```

