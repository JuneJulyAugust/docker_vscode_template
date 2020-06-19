FROM ubuntu:20.04 AS base_image

# setup bashrc
RUN cp /etc/skel/.bashrc ~/

# setup environment
ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

RUN apt-get update
RUN apt-get install -y lsb-release sudo gnupg2

# setup timezone
RUN echo 'Etc/UTC' > /etc/timezone && \
  ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime
RUN DEBIAN_FRONTEND="noninteractive" apt-get -y install tzdata


CMD ["bash"]
