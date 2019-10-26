# AusPlantScrape

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

The program will save the images into directories based first on *group*, then *family* and then *genus_species_sub.var*. Each of the species directory will contains all avliable images for that plant.Once this is done you can simply execute the program and the images will be downloaded. Image metadata will also be downloaded with the image links and photogrpaher the image is to be attributed to.

```bash
python plant_scraper.py
```

Your input plant list should be in the following format. See the `example-plant-list.csv` file.

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

## Example Output

In this example we have downloaded a set of plant images for a region devided into "native" and "introduced" for quick identification in the field.

### Direcotry file tree

```
images
├── intro
│   ├── Asteraceae
│   │   └── Sonchus_oleraceus
│   ├── Basellaceae
│   │   └── Anredera_cordifolia
│   ├── Brassicaceae
│   │   └── Cakile_maritima_subsp.\ maritima
│   ├── Caryophyllaceae
│   │   └── Polycarpon_tetraphyllum
│   ├── Poaceae
│   │   ├── Eleusine_indica
│   │   ├── Lagurus_ovatus
│   │   ├── Paspalum_dilatatum
│   │   └── Paspalum_distichum
│   └── Primulaceae
│       └── Solanum_nigrum
└── native
    ├── Apiaceae
    │   ├── Apium_prostratum_var.\ filiforme
    │   └── Centella_asiatica
    ├── Apocynaceae
    │   ├── Alyxia_buxifolia
    │   ├── Centipeda_minima_subsp.\ minima
    │   ├── Cotula_coronopifolia
    │   └── Marsdenia_rostrata
    ├── Callitrichaceae
    │   └── Callitriche_sonderi
    ├── Dicksoniaceae
    │   └── Calochlaena_dubia
    ├── Elatinaceae
    │   └── Elatine_gratioloides
    ├── Oxalidaceae
    │   └── Oxalis_corniculata
    ├── Phormiaceae
    │   └── Dianella_longifolia
    ├── Rutaceae
    │   └── Correa_alba
    ├── Scrophulariaceae
    │   ├── Limosella_australis
    │   ├── Mimulus_repens
    │   └── Veronica_plebeia
    ├── Sinopteridaceae
    │   ├── Cheilanthes_austrotenuifolia
    │   └── Pellaea_falcata_var.\ falcata
    └── Solanaceae
        └── Solanum_vescum
```

### Image set

```
images/native/Apiaceae/Centella_asiatica/
├── 0-Centella_asiatica.jpg
├── 1-Centella_asiatica.jpg
├── 2-Centella_asiatica.jpg
├── 3-Centella_asiatica.jpg
├── 4-Centella_asiatica.jpg
├── 5-Centella_asiatica.jpg
└── 6-Centella_asiatica.jpg
```

### Images

0-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/0-Centella_asiatica.jpg" width=250/>

1-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/1-Centella_asiatica.jpg" width=250/>

2-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/2-Centella_asiatica.jpg" width=250/>

3-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/3-Centella_asiatica.jpg" width=250/>

4-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/4-Centella_asiatica.jpg" width=250/>

5-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/5-Centella_asiatica.jpg" width=250/>

6-Centella_asiatica.jpg

<img src="https://github.com/Lachlan00/AusPlantScrape/blob/master/images/native/Apiaceae/Centella_asiatica/6-Centella_asiatica.jpg" width=250/>
