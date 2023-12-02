![cover.png](cover.png)
# OpenCV with cuda enabled

You can find the image on [docker hub](https://hub.docker.com/r/federicolanzani/opencv-cuda).

If you need a docker image like this one but for NVIDIA jetson, this repo has a [twin](https://github.com/lanzani/opencv-cuda-jetson-docker)!

> Feel free to open an issue if you are having some problems. 
> 
> Nvidia ecosystem can be quite difficult, I know.

**Note:** This docker image should work with every compute capability available at 2023-12-02 [here](https://developer.nvidia.com/cuda-gpus).

# What's inside the image?
- Ubuntu 18.04
- Python 3.6
- Opencv 4.8.0
- Numpy

**Details:**
- cuda version: 11.7.1
- cudnn version: 8.5

**Base Images:**
- Build: [nvidia/cuda:11.7.1-cudnn8-devel-ubuntu18.04](https://hub.docker.com/layers/nvidia/cuda/11.7.1-cudnn8-devel-ubuntu18.04/images/sha256-e135080e5e39091688102a7fef1e628183662505f02d1c71ddb9a62c0ec484c4?context=explore)
- Runtime: [nvidia/cuda:11.7.1-cudnn8-runtime-ubuntu18.04](https://hub.docker.com/layers/nvidia/cuda/11.7.1-cudnn8-runtime-ubuntu18.04/images/sha256-f5b5bf07a188573621b49758e09daeee5e4f063fab1f2e945bd48a86e6dc28e3?context=explore)


# Run
```bash
docker run -i -t --gpus=all federicolanzani/opencv-cuda bash
```

# Install

# Build




