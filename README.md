# tutorials 

## Displaying GeoTIFFs in Jupyter notebooks
Let's start with something easy.  Before diving into how to read and write raster data, how about just figuring out how to display an image, easily and by itself in Jupyter?  It turns out that this is pretty easy.

## Python
```
# JUST USE GDAL and MATPLOTLIB
from matplotlib import pyplot
%matplotlib inline
from osgeo import gdal

img = gdal.Open('test.tif').ReadAsArray()
im = pyplot.imshow(img)
```

![python_jupyter_geotif](https://user-images.githubusercontent.com/686797/69752630-780fd180-1106-11ea-92cd-dbf6d1ba4aee.png)

## R
```
# USE THE raster LIBRARY'S BUILT-IN plot() CAPABILITY
library(raster)
library(repr)

options(repr.plot.width=4, repr.plot.height=3)
img_file <- raster("test.tif")
plot(img_file)

# NOTE: repr is used solely to control the output size of the plot.  
# Without it, the image is rather large.
```

![R_jupyter_geotif](https://user-images.githubusercontent.com/686797/69753283-12bce000-1108-11ea-86c5-899ccdcd11a8.png)
