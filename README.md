##

This repository contains the processed data and the basic functions we used to estimate genetic diversity in the manuscript “Evolutionary history and past climate change shape the distribution of genetic diversity in terrestrial mammals” published in *Nature Communications*. The functions are contained in two Jupyter Notebooks and can be downloaded and run interactively together with the required input files (i.e. georeferenced and aligned genetic sequences).

##

##### Below is a basic description of the data structure in the data directory:

**Georeferenced sequences**

* data/cytb_coordinates.csv

  These are the georeferenced and spatially filtered (i.e. using species ranges) *cytb* sequences

* data/cytb_coordinates.csv

  These are the georeferenced and spatially filtered (i.e. using species ranges) *co1* sequences

**Spatial units**

* data/landGrid385.9451km.json

  This is the map that is used to map GD at the grid-cell scale (385.9451km X 385.9451km spatial resolution). The map grid was created using the chorospy library (https://github.com/spyrostheodoridis/chorospy).

* data/mammalWallaceRegionsMulti.json

This is the map that is used to map GD at the Wallace zoogeographic region scale. The map contains multiple polygones for each defined region.




