## Create a new virtual environment
```
$ conda create --name BARs python=3.10
```

Then activate the virtual environment
```
$ conda activate BARs
```

## Install PyTorch (follow [official tutorial](https://pytorch.org/get-started/locally/))
### Make sure that GPU are available on your machine and NVIDIA Driver is installed. Check your CUDA version:
```
(BARs) $ nvidia-smi | grep 'CUDA Version'
```
### Install Pytorch correspond to the CUDA version. Be patient as it may take minutes to finish the installation.
```
(BARs) $ conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
```

### Check if the pytorch with cuda is availabel in your environment. Run below python code. If your installation was successful, it should print out ``True``.
```python
import torch
torch.cuda.is_available()
```