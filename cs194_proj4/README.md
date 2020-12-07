# Facial Keypoint Detection with Neural Networks

Below are the packages need for running the notebooks

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install numpy
pip install os
pip install PyTorch
pip install pandas
pip install skimage
pip install matplotlib
pip install torchvision
pip install cv2
pip install functools
pip install math
pip install random
pip install tensorflow
```

## Usage

```python
# imports
import numpy as np

import os 
import torch
import pandas as pd
from skimage import io, transform, color
import matplotlib.pyplot as plt
from torch.utils.data import Dataset, DataLoader
import torchvision
from torchvision import transforms, utils
import torch.optim as optim

import torch.nn as nn
import torch.nn.functional as F
import cv2

import dataLoader
from dataLoader import FaceLandmarksDataset, Rescale, Rotate, ToTensor, ToGreyNormalize, ColorJitter

import functools
import math
import random
import tensorflow as tf

from models import NoseNet, FaceNet
```
