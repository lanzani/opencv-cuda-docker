#FROM nvidia/cuda:11.7.1-cudnn8-devel-ubuntu18.04
#
#ARG OPENCV_VERSION=4.8.0
#
#RUN apt-get update && apt-get upgrade -y &&\
#    # Install build tools, build dependencies and python
#    apt-get install -y \
#	    python-pip \
#        build-essential \
#        cmake \
#        git \
#        wget \
#        unzip \
#        yasm \
#        pkg-config \
#        libswscale-dev \
#        libtbb2 \
#        libtbb-dev \
#        libjpeg-dev \
#        libpng-dev \
#        libtiff-dev \
#        libavformat-dev \
#        libpq-dev \
#        libxine2-dev \
#        libglew-dev \
#        libtiff5-dev \
#        zlib1g-dev \
#        libjpeg-dev \
#        libavcodec-dev \
#        libavformat-dev \
#        libavutil-dev \
#        libpostproc-dev \
#        libswscale-dev \
#        libeigen3-dev \
#        libtbb-dev \
#        libgtk2.0-dev \
#        pkg-config \
#        ## Python
#        python-dev \
#        python-numpy \
#        python3-dev \
#        python3-numpy \
#    && rm -rf /var/lib/apt/lists/*
#
#RUN cd /opt/ &&\
#    # Download and unzip OpenCV and opencv_contrib and delte zip files
#    wget https://github.com/opencv/opencv/archive/$OPENCV_VERSION.zip &&\
#    unzip $OPENCV_VERSION.zip &&\
#    rm $OPENCV_VERSION.zip &&\
#    wget https://github.com/opencv/opencv_contrib/archive/$OPENCV_VERSION.zip &&\
#    unzip ${OPENCV_VERSION}.zip &&\
#    rm ${OPENCV_VERSION}.zip &&\
#    # Create build folder and switch to it
#    mkdir /opt/opencv-${OPENCV_VERSION}/build && cd /opt/opencv-${OPENCV_VERSION}/build &&\
#    # Cmake configure
#    cmake \
#        -DOPENCV_EXTRA_MODULES_PATH=/opt/opencv_contrib-${OPENCV_VERSION}/modules \
#        -DWITH_CUDA=ON \
#        -DCMAKE_BUILD_TYPE=RELEASE \
#        # Install path will be /usr/local/lib (lib is implicit)
#        -DCMAKE_INSTALL_PREFIX=/usr/local \
#        .. &&\
#    # Make
#    make -j"$(nproc)" && \
#    # Install to /usr/local/lib
#    make install && \
#    ldconfig
    # Remove OpenCV sources and build folder
#    rm -rf /opt/opencv-${OPENCV_VERSION} && rm -rf /opt/opencv_contrib-${OPENCV_VERSION}

FROM nvidia/cuda:11.7.1-cudnn8-devel-ubuntu18.04

ENV DEBIAN_FRONTEND=noninteractive
ENV PYTHONPATH=/usr/local/lib/python3.6/site-packages

# Install build dependencies TODO check duplicates
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y \
    nano \
    build-essential \
    cmake \
    git \
    gfortran \
    libatlas-base-dev \
    libavcodec-dev \
    libavformat-dev \
    libavresample-dev \
    libcanberra-gtk3-module \
    libdc1394-22-dev \
    libeigen3-dev \
    libglew-dev \
    libgstreamer-plugins-base1.0-dev \
    libgstreamer-plugins-good1.0-dev \
    libgstreamer1.0-dev \
    libgtk-3-dev \
    libjpeg-dev \
    libjpeg8-dev \
    libjpeg-turbo8-dev \
    liblapack-dev \
    liblapacke-dev \
    libopenblas-dev \
    libpng-dev \
    libpostproc-dev \
    libswscale-dev \
    libtbb-dev \
    libtbb2 \
    libtesseract-dev \
    libtiff-dev \
    libv4l-dev \
    libxine2-dev \
    libxvidcore-dev \
    libx264-dev \
    pkg-config \
    python-dev \
    python-numpy \
    python3-dev \
    python3-numpy \
    python3-matplotlib \
    qv4l2 \
    v4l-utils \
    zlib1g-dev \
    python-pip \
    build-essential \
    cmake \
    git \
    wget \
    unzip \
    yasm \
    pkg-config \
    libswscale-dev \
    libtbb2 \
    libtbb-dev \
    libjpeg-dev \
    libpng-dev \
    libtiff-dev \
    libavformat-dev \
    libpq-dev \
    libxine2-dev \
    libglew-dev \
    libtiff5-dev \
    zlib1g-dev \
    libjpeg-dev \
    libavcodec-dev \
    libavformat-dev \
    libavutil-dev \
    libpostproc-dev \
    libswscale-dev \
    libeigen3-dev \
    libtbb-dev \
    libgtk2.0-dev \
    pkg-config \
    python-dev \
    python-numpy \
    python3-dev \
    python3-numpy \
    libeigen3-dev

RUN mkdir "build_opencv"

COPY build_opencv.sh build_opencv/

RUN cd build_opencv && ./build_opencv.sh
