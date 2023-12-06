FROM nvidia/cuda:11.7.1-cudnn8-runtime-ubuntu18.04

ENV DEBIAN_FRONTEND=noninteractive
ENV PYTHONPATH=/usr/local/lib/python3.6/site-packages

# Install runtime dependencies
RUN apt-get update && apt-get upgrade -y --autoremove && \
    apt-get install -y \
    python3-dev \
    python3-pip \
    python3-numpy \
    libfreetype6 \
    libharfbuzz0b \
    libgstreamer1.0-0 \
    libglib2.0-0 \
    libgstreamer-plugins-base1.0-0 \
    libtesseract4 \
    libgtk-3-0 \
    libgdk-pixbuf2.0-0 \
    libdc1394-22 \
    libavcodec57 \
    libavformat57 \
    libswscale4 \
    liblapack3 \
    libatlas3-base && \
    apt-get clean

COPY installer/OpenCV-4.8.0-x86_64.sh ./opt

RUN cd /opt && ./OpenCV-4.8.0-x86_64.sh --prefix=/usr/local --skip-license --exclude-subdir

#RUN echo opencv_version
#RUN python3 -c "import cv2; print('OpenCV version:', str(cv2.__version__)); print(cv2.getBuildInformation())"
