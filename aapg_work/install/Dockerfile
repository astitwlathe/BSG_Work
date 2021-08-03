FROM ubuntu:18.04

WORKDIR /usr/src/aapg

RUN apt-get update && apt-get install -y \ 
	git	\
	python3.7 \
	python3-setuptools \
	python3-pip \
	libpython3.7-dev

# Clone and move into project directory

RUN git clone https://gitlab.com/shaktiproject/tools/aapg 

# Packages for python install
RUN python3.7 -m pip install pyyaml

RUN python3.7 -m pip install pytest

# python setup
RUN cd aapg; python3.7 setup.py install

# May or may not be required due to custom yaml script
# RUN aapg setup 

CMD ["bash"]

