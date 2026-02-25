# A toolbox to map shrub cover and biomass from drone data

_This toolbox was developped to enable the derivation of the common habitat condition metric'shrub cover' using drone imagery or airborne LiDAR data. Funded by MAMBO (Modern Approaches to the Monitoring of Biodiversity), an EU Horizon project_ 

The toolbox contains open-source software and notes that enable you to map individual shrub crowns from drone imagery using a deep learning model. It also provides you with an allometric model that estimates individual shrub biomass from shrub crown diameter and height. Both deep learning and allometry model are at development stage. 

* The software package [attn-unet-shrub-id](https://github.com/MAMBO-Habitat/attn-unet-shrub-id) maps individual shrub crowns using 2-dimensional drone image mosaics as input. It contains a deep learning model (U-NET) that was trained using labelled images collected from drone imagery of a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   
* Related to the U-NET model is the software called [shrub-prepro](https://github.com/MAMBO-Habitat/shrub-prepro) is a Python package and CLI for pre-processing geospatial data to support the generation of labelled images: 
   * Creating binary masks from shapefiles. 
   * Generating rotated versions of processed images (to increase number of labelled images). 
   * Combining RGB imagery with DSM data into processed samples. 
* [workshops](https://github.com/MAMBO-Habitat/workshops) contains Jupiter notebooks and slides which guide you through the steps to
    * prepare training data using shrub-prepro, 
    * train the U-NET model using attn-unet-shrub-id 
    * run the U-NET model using attn-unet-shrub-id to produce a shrub map classification.
* [metadata](https://github.com/MAMBO-Habitat/metadata) contains a list of downloadable files (e.g., drone image mosaics, lidar las files, U-Net labelled images and more)

The biomass model called [BRAMBLE](https://github.com/MAMBO-Habitat/BRAMBLE) is designed to be trained with incomplete data. The test case uses destructive samples of Hawthorn shrubs collected in a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   

The lead organisation for this work is [UK Centre for Ecology and Hydrology](https://github.com/NERC-CEH/)

MAMBO receives funding from the European Union's Horizon Europe research and innovation programme under grant agreement No.101060639.
