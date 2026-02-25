# MAMBO (Modern Approaches to the Monitoring of Biodiversity)

_Develop consistent and standardised habitat condition metrics using state of the art drone imagery or airborne LiDAR and integrating the data into a deep learning framework._ 

The toolbox contains open-source software and notes that enable you to map individual shrub crowns from drone imagery using a deep learning model. It also provides you with an allometric model that estimates individual shrub biomass from shrub crown diameter and height. Both deep learning and allometry model are at development stage. 

* The software called attn-unet-shrub-id maps individual shrub crowns using 2-dimensional drone image mosaics as input. It contains a deep learning model (U-NET) that was trained using labelled images collected from drone imagery of a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   
* Related to the U-NET model is the software called shrub-prepro is a Python package and CLI for pre-processing geospatial data to support the generation of labelled images: 
* Creating binary masks from shapefiles. 
* Generating rotated versions of processed images (to increase number of labelled images). 
* Combining RGB imagery with DSM data into processed samples. 
* workshops contains Jupiter notebooks which guide you through the steps to
    * prepare training data using shrub-prepro, 
    * train the U-NET model using attn-unet-shrub-id 
    * run the U-NET model using attn-unet-shrub-id to produce a shrub map classification.   

The biomass model called BRAMBLE is designed to be trained with incomplete data. The test case uses destructive samples of Hawthorn shrubs collected in a rewilding site in the UK, managed by the Wildlife Trust (Strawberry Hill farm, Bedfordshire).   

 

Main novelty 

The main novelty lies in a U-NET deep learning model trained to identify (Hawthorn) shrubs and a Maximum Entropy allometric model using Bayesian inference developed to be trained with incomplete data.  

 

Scale 

    Spatial: Local, site based monitoring 

    Temporal: Single date or Repeat visits 

    Thematic: Habitat condition metric (shrub cover & biomass) relevant to biodiversity monitoring and ecosystem assessment 

 

Potential outcomes & impact 

    Enhanced evidence base for biodiversity assessments, conservation planning and environmental reporting 

    Support to EU and national policy frameworks (e.g. biodiversity strategies, habitat reporting) 

    Increased uptake of UAV-derived products by public authorities and research communities 

 

Accessible by 

Everyone.  

 

Accessible via 

Github repository  https://github.com/MAMBO-Horizon-WP4 

 

Users 

Potential users are researchers, land managers and conservation practitioners, and private sector actors involved in environmental monitoring and ecosystem assessment. Examples: 

    National and regional environmental authorities 

    Biodiversity and ecosystem researchers 

    Conservation NGOs 

    Environmental consultancies and service providers 

 

User exploitation beyond the project 

Users can further develop and train the models to suit their local shrub mapping requirements  

 

Barriers to exploitation and mitigation measures 

    Barrier: Expertise in coding in python and Jupyter notebooks is essential to take advantage of this toolbox 
    Mitigation: Documentation provided 

    Barrier: Both deep learning and allometry model are at development stage 
    Mitigation: free availability on github will enable future development 

    Barrier: Limited awareness  
    Mitigation: Targeted communication, demonstrations and user-oriented documentation 

 

Further development by partners beyond the project 

Partners plan to further develop and maintain the workflows, making it more user friendly and improving the allometry model. 

 

Potential communication activities to support exploitation 

    Dedicated project web pages highlighting the workflow and datasets 

    Webinars and training demonstrating the toolbox 

    Scientific publications and conference presentations 

    Training materials and use-case examples targeting practitioners 

 

The lead organisation for this objective is [UK Centre for Ecology and Hydrology](https://github.com/NERC-CEH/)

MAMBO receives funding from the European Union's Horizon Europe research and innovation programme under grant agreement No.101060639.
