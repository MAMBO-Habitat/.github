# A toolbox to map shrub cover and biomass from drone data

_Develop consistent and standardised habitat condition metrics using state of the art drone imagery or airborne LiDAR and integrating the data into a deep learning framework. Funded by MAMBO (Modern Approaches to the Monitoring of Biodiversity), an EU Horizon project_ 

The toolbox contains open-source software and notes that enable you to map individual shrub crowns from drone imagery using a deep learning model. It also provides you with an allometric model that estimates individual shrub biomass from shrub crown diameter and height. Both deep learning and allometry model are at development stage. 

* The software package [attn-unet-shrub-id](https://github.com/MAMBO-Habitat/attn-unet-shrub-id) maps individual shrub crowns using 2-dimensional drone image mosaics as input. It contains a deep learning model (U-NET) that was trained using labelled images collected from drone imagery of a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   
* Related to the U-NET model is the software called [shrub-prepro](https://github.com/MAMBO-Habitat/shrub-prepro) is a Python package and CLI for pre-processing geospatial data to support the generation of labelled images: 
* Creating binary masks from shapefiles. 
* Generating rotated versions of processed images (to increase number of labelled images). 
* Combining RGB imagery with DSM data into processed samples. 
* [workshops](https://github.com/MAMBO-Habitat/workshops) contains Jupiter notebooks which guide you through the steps to
    * prepare training data using shrub-prepro, 
    * train the U-NET model using attn-unet-shrub-id 
    * run the U-NET model using attn-unet-shrub-id to produce a shrub map classification.   

The biomass model called BRAMBLE is designed to be trained with incomplete data. The test case uses destructive samples of Hawthorn shrubs collected in a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   

## Main novelty 

The main novelty lies in a U-NET deep learning model trained to identify (Hawthorn) shrubs and a Maximum Entropy allometric model using Bayesian inference developed to be trained with incomplete data.  

## Scale 

* Spatial: Local, site based monitoring
* Temporal: Single date or Repeat visits 
* Thematic: Habitat condition metric (shrub cover & biomass) relevant to biodiversity monitoring and ecosystem assessment 

The lead organisation for this objective is [UK Centre for Ecology and Hydrology](https://github.com/NERC-CEH/)

MAMBO receives funding from the European Union's Horizon Europe research and innovation programme under grant agreement No.101060639.
