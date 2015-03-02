#
# Dockerfile for python setup
#
# https://github.com/rajalokan/dockerfiles/python
#

# Pull base image.
FROM rajalokan/ubuntu
MAINTAINER "Alok Kumar <rajalokan@gmail.com>"

# Install Python.
RUN \
  apt-get update && \
  apt-get install -y python python-dev && \
  rm -rf /var/lib/apt/lists/*

# Upgrade to latest pip
RUN wget https://bootstrap.pypa.io/get-pip.py -P /tmp/
RUN python /tmp/get-pip.py

# Install basic python packages
RUN pip install virtualenv ipython

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["bash"]
