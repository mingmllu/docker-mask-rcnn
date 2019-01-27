## The Dockerized implementation of Mask R-CNN 

Please find [here](https://github.com/mingmllu/Mask_RCNN) the details of the Mask R-CNN implementation for instance segmentation.

### Prerequisites for host machine

* Ubuntu 16.04 LTS 
* Nvidia GPU and [software](https://www.tensorflow.org/install/gpu) installed
* Install Docker version 18.06 or higher
* Install [Nvidia-Docker](https://github.com/NVIDIA/nvidia-docker)
* Install docker-compose version 1.23.2 or higher

### Create a virtual environment for client

You can do this on a separate client machine (Linux or Windows) or the host machine.

The client and host machines must be connected to the same network.

* Create a virtual environmrnt: ```virtualenv --python=python3.5 _venv3.5```
* Activate the virtual environment
* Run ```pip3 install -r requirments.txt``` to install the required packages

### Create and start the Mask R-CNN container on the host GPU machine

```
$ docker-compose up
```

### Start Zero-MQ client to show processed images

```
python video_zmq_client.py --server-ip xxx.xxx.xxx.xxx --port 5566
```
where xxx.xxx.xxx.xxx is the IP address of the GPU host machine where the container is runnig.
