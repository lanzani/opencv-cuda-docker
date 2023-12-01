![cover.png](cover.png)
# OpenCV with cuda

You can find the image on [docker hub](https://hub.docker.com/r/federicolanzani/opencv-cuda).

If you need a docker image like this one but for NVIDIA jetson, this repo has a [twin](https://github.com/lanzani/opencv-cuda-jetson-docker)!

> Feel free to open an issue if you are having some problems. 
> 
> Nvidia ecosystem can be quite difficult, I know.

# Run
```bash
docker run -i -t --gpus=all federicolanzani/opencv-cuda bash
```

# Install

# Build


-> note on compute capability:
https://developer.nvidia.com/cuda-gpus

https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#compute-capabilities



ubuntu 18.04, cuda 11.7.1, cudnn8.5
Base Image: 
nvidia/cuda:11.7.1-cudnn8-runtime-ubuntu18.04