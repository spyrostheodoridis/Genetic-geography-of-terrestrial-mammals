##

This repository contains the processed data and the basic functions to estimate genetic diversity as described in the paper “Evolutionary history and past climate change shape the distribution of genetic diversity in terrestrial mammals” published in *Nature Communications*. The functions are contained in two Jupyter Notebooks and can be downloaded and run interactively together with the required input files (i.e. georeferenced and aligned genetic sequences).

##

The user should first run the AssignSequencesToUnits.ipynb Jupyter Notebook by selecting the desired marker. After the assignment of sequences to spatial units the user can run the second Notebook to estimate GD per spatial unit.

##

### Below is a basic description of the data structure in the data directory:

##

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

**Aligned sequences**

* data/mammals_cytb.zip

  This is a directory containing all sequence alignments (fasta format) per species for *cytb*. It should be unzipped to be used with the python notebooks.

* data/mammals_co1.zip

  This is a directory containing all sequence alignments (fasta format) per species for *co1*. It should be unzipped to be used with the python notebooks.

**Climate data**

* data/past_climate
  
  This directory contains the processed paleoclimate data that were used to estimate past climate change / stability as predictor for GD. The four files represent temperature and precipitation trend and variability within extreme centuries of temperature change since the Last glacial Maximum. 
  
  
  

