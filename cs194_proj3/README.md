# Project 3: Face Morphing

## Imports

You will need the following imports

```bash
pip install matplotlib
pip install skimage
pip install scipy
pip install multiprocessing
```

## Usage
```python
#imports
import matplotlib
matplotlib.use('TkAgg')
matplotlib.interactive(True)

import math
import numpy as np
import matplotlib.pyplot as plt
import skimage.transform as sktr
import skimage.draw as draw

#for triangluation
from scipy.spatial import Delaunay
from numpy import linalg
from scipy import interpolate

#this import is not necessary unless working with large images (>3000x3000)
import multiprocessing
```
