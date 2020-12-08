
# FROM osrf/ros:melodic-desktop-full-bionic
FROM tiryoh/ros-desktop-vnc:melodic-cuda-10.2
# cmake
RUN cd /opt/ \
    && curl -L https://github.com/Kitware/CMake/releases/download/v3.17.1/cmake-3.17.1-Linux-x86_64.tar.gz  --output cmake.tar.gz \
    && tar -xvzf cmake.tar.gz \
    && rm cmake.tar.gz \
    && rm -f /usr/bin/cmake \
    && rm -f /usr/bin/ctest \
    && update-alternatives --install /usr/bin/cmake cmake /opt/cmake-3.17.1-Linux-x86_64/bin/cmake 60 --slave /usr/bin/ctest ctest /opt/cmake-3.17.1-Linux-x86_64/bin/ctest



RUN apt-get update \
    && apt-get install -y software-properties-common \
    && add-apt-repository ppa:ubuntu-toolchain-r/test -y\
    && apt update \
    && apt install g++-7 -y \
    && update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 60 --slave /usr/bin/g++ g++ /usr/bin/g++-7 \
    && update-alternatives --config gcc \
    && apt install -y python-pip \
    && pip install cpplint \
    && apt install -y lcov \
    && apt install -y cppcheck \
    && apt install -y curl \
    && apt install -y unzip \
    && apt install -y doxygen \
    && apt install -y graphviz \
    && apt install -y clang-format

RUN apt-get install ros-melodic-jsk-recognition-msgs -y


CMD ["echo", "Successfully load the docker image"]
