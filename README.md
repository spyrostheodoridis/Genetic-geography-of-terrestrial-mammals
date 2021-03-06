##

This repository contains the processed data and the basic functions to estimate genetic diversity as described in the paper “Evolutionary history and past climate change shape the distribution of genetic diversity in terrestrial mammals” published in *Nature Communications*. The functions are contained in a Jupyter Notebook and can be downloaded and run interactively together with the required input files (i.e. georeferenced and aligned genetic sequences).

##

### Below is a description of the data structure in the data directory:

##

**Georeferenced sequences**

* data/cytb_coordinates.csv

  These are the georeferenced and spatially filtered (i.e. using species ranges) *cytb* sequences.

* data/cytb_coordinates.csv

  These are the georeferenced and spatially filtered (i.e. using species ranges) *co1* sequences.

**Spatial units**

* data/landGrid385.9451km.json

  This is the grid that is used to map GD at the grid cell scale (385.9451km x 385.9451km spatial resolution). The grid (Behrmann Cylindrical Equal-Area Projection) was created using the chorospy library (https://github.com/spyrostheodoridis/chorospy).

* data/mammalWallaceRegionsMulti.json

  This is the map that is used to map GD at the Wallace zoogeographic region scale. The map contains multiple polygones for each defined region.
  
**Assigned sequences**

* data/assigned_sequences

  This directory contains the python dictionaries that should be used to estimate genetic diversity per spatial unit. the dictionaries store the sequence ids per species and spatial unit.
 

**Aligned sequences**

* data/mammals_cytb.zip

  This is a directory containing all sequence alignments (fasta format) per species for *cytb*. It should be unzipped to be used with the python notebook.

* data/mammals_co1.zip

  This is a directory containing all sequence alignments (fasta format) per species for *co1*. It should be unzipped to be used with the python notebook.

**Climate data**

* data/past_climate
  
  This directory contains the processed paleoclimate data that were used to estimate past climate change / stability as predictor for GD. The four files represent temperature and precipitation trend and variability within extreme centuries of temperature change since the Last Glacial Maximum. 
  
 
**Processed data**
  
* data/processed_data

  This directory contains all the processed data needed to reproduce the statistical analyses and generate the figures in the paper. The .csv files are the dataframes that contain the observed genetic diversity to gether with all the independant variables, plus additional information necessary to filter the data. Below is the description of the columns of the file. Each row in the file represents a spatial unit (i.e. grid-cell or zoogeographic region).
  
  - The first unnamed column is the spatial unit identity
  - xC,yC: The geographic coordinates of the cell centroid. This information is missing at the zoogeographic region scale
  - GD: The average genetic diversity across all sampled species
  - mammalTaxa: The total number of sampled species
  - mammalSeqs: The total number of sampled sequences
  - meanSeqs: Mean number of sequences per species
  - Dist: The mean geographic distance across all sampled sequences
  - PD: Phylogenetic diversity
  - nTaxa: Species richness
  - GlobalExtreme_prTrendExt,GlobalExtreme_prVarExt,GlobalExtreme_tsTrendExt,GlobalExtreme_tsVarExt: Precipitation (pr) and temperature (ts) trend and variability.
  - kk10: Anthropogenic land-use change during the Holocene
  - HFP2009: Human footprint at 2009
  - GDsqrt: The square root of genetic diversity
  - TaxonComplete: Taxonomic coverage (sampled species divided by species richness)

  The cytb_grid_orders.csv and co1_grid_orders.csv files contain a summary of genetic diversity per grid cell at the mammal order level.

* data/predicted_GD
  
  This directory contains the two predicted maps of genetic diversity presented in Figure 3. The maps were created using the strabo library (https://github.com/spyrostheodoridis/strabo) and d3.js (https://d3js.org/)
