# I2K2022-SIM
I2K 2022 mcSIM tutorial


## Install mcSIM package
Create and activate a new conda environment.
```
conda create -n mcsimi2k python=3.9
conda activate mcsimi2k
```

Install mcSIM package and Napari via pip.
```
pip install "git+https://git@github.com/qi2lab/mcSIM@master#egg=mcSIM" "napari[all]"
````
## Download example 2D-SIM data
Resolution target 2D-SIM:

*Argolight SIM slide v1*

*Instrument: qi2lab DMD-SIM*

Tetrahymena two color immunofluorescence 2D-SIM z stack:

*Sample prepared by Dr. Nick Galati at [Western Washington University](https://wp.wwu.edu/galatilab/)*

*Instrument: qi2lab DMD-SIM*

Nikon N-SIM three color immunofluorescence 2D-SIM image:

*Sample prepared and data generated by Dr. Christophe Leterrier at [NeuroCyto Lab](https://www.neurocytolab.org/)*

*Instrument: Nikon N-SIM*

## Explore examples
Example notebooks that explore reconstruction for each dataset are provided in `/examples`
