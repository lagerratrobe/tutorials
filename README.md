# tutorials 

## Displaying GeoTIFFs in Jupyter notebooks
Let's start with something easy.  Before diving into how to read and write raster data, how about just figuring out how to display an image, easily and by itself in Jupyter.  It turns out that this is pretty easy.

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

img_file <- raster("test.tif")
plot(img_file)
```

![R_jupyter_geotif](https://user-images.githubusercontent.com/686797/69752640-7e9e4900-1106-11ea-8dfa-e833be74e62a.png)
