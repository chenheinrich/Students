# Setup on TACC
(Last Updated: May 2019)   

## Access and usage on TACC
1. Create an account on [TACC] (https://portal.tacc.utexas.edu/) and email [Bryan Bales](bryan.a.bales@jpl.nasa.gov) to get approved access to Stampede2 (CPUs) and Maverick2 (GPUs) following instructions. 
2. Store data, install software etc. in work instead of home (there you have permission, e.g. `pip3 install --user` ...)
3. TACC has great documentations:  
https://portal.tacc.utexas.edu/user-guides/stampede2#using-citizenship  
https://portal.tacc.utexas.edu/user-guides/maverick2  

## Setup Tensorflow and Keras 
1. Follow [TACC page](https://portal.tacc.utexas.edu/software/tensorflow) for installing tensorflow on Maverick2, but replace  
`pip install --user tensorflow-gpu` (which installs the latest version) with  
`python3 -m pip install --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.13.1-cp37-cp37m-linux_x86_64.whl --user` (Info: https://www.tensorflow.org/install/pip).  
This will install tensorflow-gpu 1.12.0, which is compatible with the cuda version available on Maverick2.   
3. Replace `module load cuda/9.0 cudnn/7.0` with `module load cuda/9.0 cudnn/7.4.2`.  
4. Use `module load intel/17.0.4` before running.  
