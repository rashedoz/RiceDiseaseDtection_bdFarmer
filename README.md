# Plant Disease Detection

This projects consists of two parts.

  - Cloud ML Sererver
  - Android App

# Project Overview
Overall System Architecture:

![Architecture](Figures/system.png?raw=true "Architecture")


# Android App
Android Screenshots:

![Screenshot](Figures/screenshots.png)



# Cloud Server
There are two different servers available. Either one of the server running needs to be running.
  - Django based Server
  - Flask based server
  
# Flask Server
install flask via pip and all the dependencies.
```sh
pip install flask
```
# Flask Server running model
Running flask model->
1. Start and run google instance.
2. Activate project env "source activate tf_cpu"
3. cd to Flask Server folder.
3. Run "python3 flask\ model.py"
4. Goto instance ip:5000 (e.g http://35.244.41.56:5000/)
5. Keep the tab open all the time.
6. New images are sent to firebase.
7. As new images are sent the page will auto reload and the prediction will be sent to firebase as output.




# Running Environment

#Docker 
# Assuming an Ubuntu Docker image
$ docker run -it <image> /bin/bash
	
Kaggle -> 

Dropmark Links-> https://rashedoz.dropmark.com/592180


GCP Steps->

Cmd:


```
source activate tf_gpu
jupyter-notebook --no-browser --port=8123
```


(tf_gpu) yaan_uchiha29@r-gpu:~$


Tensorboard:
```
	tensorboard --logdir='logs/'
```

SSH:
```
ssh -i [PATH_TO_PRIVATE_KEY] [USERNAME]@[EXTERNAL_IP_ADDRESS]

//create key-pair
ssh-keygen -C yaan_uchiha29

```

Notebook:

Running Notebook:
jupyter-notebook --no-browser --port=8123

Jupyter notebook different python executable solve:
	python3 -m ipykernel install --user



install Nvidia's CUDA software:


# update apt-get
sudo apt-get update
 
# work as root
sudo su

#!/bin/bash
echo "Checking for CUDA and installing."
# Check for CUDA and try to install.
if ! dpkg-query -W cuda; then
    curl -O https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cuda-repo-ubuntu1604_9.0.176-1_amd64.deb
    sudo dpkg -i cuda-repo-ubuntu1604_9.0.176-1_amd64.deb
    sudo apt-get update
    sudo apt-get install cuda-9-0
    sudo nvidia-smi -pm 1


Test that your GPU is successfully installed:
# check that GPU is working
Nvidia-smi




Install cudnn and tensorflow gpu using anaconda:
conda create --name tf_gpu tensorflow-gpu


If cudnn not installed then:
 
Install your Deep Neural Network (cuDNN) binaries that you uploaded earlier (check your version):
sudo dpkg -i libcudnn7_7.1.4.18-1+cuda9.0_amd64.deb //download cuDNN runtime library




Set sticky path defaults
echo 'export CUDA_HOME=/usr/local/cuda' >> ~/.bashrc
echo 'export PATH=$PATH:$CUDA_HOME/bin' >> ~/.bashrc
echo 'export LD_LIBRARY_PATH=/usr/local/cuda/extras/CUPTI/lib64:$LD_LIBRARY_PATH' >> ~/.bashrc
source ~/.bashrc




	



License
----

