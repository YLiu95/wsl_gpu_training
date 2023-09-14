# gpu training with wsl

Run the following commands to update and upgrade the packages
```diff
sudo apt update
```


```diff
sudo apt upgrade
```

install python3-pip 
```diff
sudo apt install python3-pip
```

verify the installation of python3-pip
```diff
pip3 --version
```

#### below code are from tensorflow tutorial 
https://www.tensorflow.org/install/pip#windows-wsl2 

**make sure you can see this:**

try open the link on a personal pc with incognito mode in Google Chrome
![image](https://github.com/YLiu95/wsl_gpu_training/assets/82934216/a93e1bdc-ba36-47e0-b68b-694586880ebe)


**follow prof Jeff Heaton's tutorial**

https://youtu.be/0S81koZpwPA?si=rlfjOImuGVyOn6_-

Install Miniconda
```diff
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o Miniconda3-latest-Linux-x86_64.sh
```


```diff
bash Miniconda3-latest-Linux-x86_64.sh
```

Create a conda environment
```diff
conda create --name tf python=3.9
```


```diff
conda activate tf
```

verify GPU driver
```diff
nvidia-smi
```

Install CUDA and cuDNN with conda and pip.
```diff
conda install -c conda-forge cudatoolkit=11.8.0
```

```diff
pip install nvidia-cudnn-cu11==8.6.0.163
```

```diff
mkdir -p $CONDA_PREFIX/etc/conda/activate.d
```

```diff
echo 'CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
```

```diff
echo 'export LD_LIBRARY_PATH=$CUDNN_PATH/lib:$CONDA_PREFIX/lib/:$LD_LIBRARY_PATH' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
```

```diff
pip install --upgrade pip
```

```diff
pip install tensorflow==2.13.*
```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```

```diff

```
