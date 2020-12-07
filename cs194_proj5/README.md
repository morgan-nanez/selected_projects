# Project 5.1



## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install matplotlib
pip install numpy
pip install skimage
pip install cv2
```

## Usage

```python
import matplotlib
matplotlib.use('TkAgg')
matplotlib.interactive(True)
import matplotlib.pyplot as plt

plt.imshow(image)
im1_pts = plt.ginput(num_points)
```

```python
import numpy as np
from numpy import linalg

#apply least squares
H = np.linalg.lstsq(A, b.T)

#matrix math
H_inv = np.linalg.inv(H)
dot_product = H_inv.dot(indices)
```

```python
import skimage.transform as sktr
import skimage.draw as draw
import skimage.io as io

#loading images
image = io.imread(image_path)
```

```python
import cv2

#remap to get color during transformations
warped_im = cv2.remap(im1, map_x, map_y, cv2.INTER_LINEAR)
```