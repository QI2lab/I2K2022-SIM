# I2K 2022 tutorial on High quality 2D SIM reconstruction in python with mcSIM

## I2K 2022 video tutorial
[![I2K 2022 video tutorial](https://user-images.githubusercontent.com/26783318/166836402-b81c7d1e-b7c5-4586-9e4d-e61b2e68c728.png)](http://www.youtube.com/watch?v=mDar-MjMtW0 "I2K 2022 video tutorial")

## Conda environments
The installation instructions assume you have a conda environment. If you have never used conda before, please [read this guide first](https://biapol.github.io/blog/johannes_mueller/anaconda_getting_started/).

## Install mcSIM package
Create a new conda environment.
```
conda create -n mcsimi2k python=3.9
```
Activate the new conda environment.
```
conda activate mcsimi2k
```

Install [mcSIM](https://github.com/QI2lab/mcSIM) package, [Napari](https://napari.org/), and other required tutorial packages via pip (roughly 5-10 minutes install).
```
pip install "git+https://git@github.com/qi2lab/mcSIM@master#egg=mcSIM" "napari[all]" "nd2" "ipykernel" "ipympl" "napari-plot-profile"
````

Depending on how you plan to interact with the Jupyter Notebooks (VS Code, PyCharm, JupyterLab, etc..) you may need to perform additional installs.

For example, if you want to use [JuypterLab](https://jupyterlab.readthedocs.io/en/stable/) to run the notebooks, you need to install it using,

```
pip install jupyterlab
```

## Download the reconstruction examples in this repository
```
git clone https://github.com/QI2lab/I2K2022-SIM.git
```

If you don't have git installed, you can download this repository using the green code button above and unzip on your computer.

## Download example 2D-SIM data

[Download example data archive](https://drive.google.com/file/d/1MaWGsRvqyV1nLH7wb8afDcK5edQcEhHk/view?usp=sharing) (~1.6 gigabytes). Unzip into directory where you cloned this repository.
**IMPORTANT**: During the video, we reference that some files are stored as pickle files by mcSIM. To ensure that there are no security issues, we replaced all pickle code and files with json code and files. Please ignore this discussion in the videos. Thank you!

### Example 1: Calibrating spatial light modulator
*Uniform dye slide*

*Instrument: qi2lab DMD-SIM*

### Example 2: Reconstruction parameters: Resolution target 2D-SIM

![Clipboard-1](https://user-images.githubusercontent.com/26783318/166563449-ee752ecd-fd03-47a3-be4c-ea37910aef68.png)

*Argolight SIM slide v1*

*Instrument: qi2lab DMD-SIM*

### Example 3: Optical sectioning: Tetrahymena immunofluorescence 2D-SIM z stack

![tet-sim](https://user-images.githubusercontent.com/26783318/166161389-6a4bd0ec-57c9-4717-b451-e60293319119.gif)

*Sample prepared by Dr. Nick Galati at [Western Washington University](https://wp.wwu.edu/galatilab/)*

*Instrument: qi2lab DMD-SIM*

### Example 4: Uncalibrated modulators: Nikon N-SIM three color immunofluorescence 2D-SIM image

![Comparison-1](https://user-images.githubusercontent.com/26783318/166563379-19bc1766-814b-4e55-9add-f7dbd5ceab61.png)

*Sample prepared and data generated by Dr. Christophe Leterrier at [NeuroCyto Lab](https://www.neurocytolab.org/)*

*Instrument: Nikon N-SIM*
