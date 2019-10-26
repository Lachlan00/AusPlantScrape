# AusPlantScrape

## About

A program to download low resolution images from the Australian Plant Image Index on the Australian National Botanical Gardens webpage. As of 2019-Oct-26, non-commercial use of low-resolution images downloaded from the Photo Collection area of the website is allowed on condition that the photographer is credited by name, if known, and that the copyright holder is also acknowledged. The source of the image should be listed as the Australian National Botanic Gardens and these words linked to the Photo Collection home page, http://www.anbg.gov.au/photo. For more up to date information on licensing visit: https://www.anbg.gov.au/photo/photo-collection-use.html

> Non-commercial use of low-resolution images downloaded from the Photo Collection area of our website is allowed on condition that the photographer is credited by name, if known, and that the copyright holder is also acknowledged. The source of the image should be listed as the Australian National Botanic Gardens and these words linked to our Photo Collection home page, http://www.anbg.gov.au/photo.
*Source - [Australian National Botanical Gardens webpage](https://www.anbg.gov.au/photo/photo-collection-use.html) 2019-Oct-26*

## How To Use

To use this program simply download the repository and edit the `config.py` file and specify your plant list CSV file and the directory you wish the images to be saved to.

```python
# configuration
plant_list = './data/example-plant-list.csv' # file path of input plant list
base_dir = './images/' # where you want to save the images to
```
Your plant list should be in the following format:

group | family | genus | species | sub.var
--- | --- | --- | --- | ---
native | Apiaceae | Apium | prostratum | var. filiforme
native | Elatinaceae | Elatine | gratioloides | NA
native | Oxalidaceae | Oxalis | corniculata | NA
native | Phormiaceae | Dianella | longifolia | NA
native | Poaceae | Agrostis | avenacea | var. avenacea
native | Rutaceae | Correa | alba | NA
native | Scrophulariaceae | Limosella | australis | NA
native | Sinopteridaceae | Cheilanthes | austrotenuifolia | NA
native | Solanaceae | Solanum | vescum | NA
intro | Asteraceae | Sonchus | oleraceus | NA
intro | Basellaceae | Anredera | cordifolia | NA
intro | Brassicaceae | Cakile | maritima | subsp. maritima
intro | Poaceae | Lagurus | ovatus | NA
intro | Poaceae | Paspalum | dilatatum | NA

The program will save the images into directories based first on *group*, then *family* and then *genus_species_sub.var*. Each of the species directory will contains all avliable images for that plant. 