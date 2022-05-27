# I2K 2022 tutorial on High quality 2D SIM reconstruction in python with mcSIM

## I2K 2022 video tutorial  
[![I2K 2022 video tutorial](https://user-images.githubusercontent.com/26783318/166836402-b81c7d1e-b7c5-4586-9e4d-e61b2e68c728.png)](http://www.youtube.com/watch?v=mDar-MjMtW0 "I2K 2022 video tutorial")

After the I2k conference, we added "Example 5 - oblique plane structured illumination microscopy". There is not currently a video walkthrough available for this example.

## Conda environments  
The installation instructions assume you have a conda environment. If you have never used conda before, please [read this guide first](https://biapol.github.io/blog/johannes_mueller/anaconda_getting_started/).

## Create mcSIM python environment  
Create a new conda environment.
```
conda create -n mcsimi2k python=3.10
```
Activate the new conda environment.
```
conda activate mcsimi2k
```

Install [mcSIM](https://github.com/QI2lab/mcSIM) package, [Napari](https://napari.org/), and other required tutorial packages via pip (roughly 5-10 minutes install).
```
pip install "git+https://git@github.com/qi2lab/mcSIM@master#egg=mcSIM" "napari[all]" "nd2" "ipykernel" "ipympl" "numba" "itk-elastix"
````

Depending on how you plan to interact with the Jupyter Notebooks (VS Code, PyCharm, JupyterLab, etc..) you may need to perform additional installs.

For example, if you want to use [JuypterLab](https://jupyterlab.readthedocs.io/en/stable/) to run the notebooks, you need to install it using,

```
pip install jupyterlab
```
 
Some mcSIM functions can be optionally run on a GPU. If this is desired, ensure your python environment has the [appropriate version of CuPy](https://cupy.dev/) installed. mcSIM will automatically utilize the GPU if CuPy is installed and working.

## Download the reconstruction example notebooks and resources  
```
git clone https://github.com/QI2lab/I2K2022-SIM.git
```

If you don't have git installed, you can download this repository using the green code button above and unzip on your computer.

## Download example 2D-SIM data  

[Download example data archive](https://drive.google.com/file/d/1MaWGsRvqyV1nLH7wb8afDcK5edQcEhHk/view?usp=sharing) (~1.6 gigabytes). Unzip into directory where you cloned this repository.  
**IMPORTANT**: During the video, we reference that some files are stored as pickle files by mcSIM. To ensure that there are no security issues, we replaced all pickle code and files with json code and files. Please ignore this discussion in the videos. Thank you!

**For Example 5 only**: The raw data for oblique plane structured illumination microscopy must to be downloaded from the [Zenodo archive](https://zenodo.org/record/6481084#.YmVM-7lOmHs) provided with the [preprint](https://www.biorxiv.org/content/10.1101/2022.05.19.492671v1.full). Full instructions are provided in the example notebook.

### Example 1. Calibrating spatial light modulator

![Figure 1-1](https://user-images.githubusercontent.com/26783318/167058036-15de7af4-ac36-4ade-aa24-92e5880509d3.png)

*Sample: Uniform dye slide*  
*Prepared by: Dr. Peter Brown at qi2lab*  
*Imaged by: Dr. Peter Brown at qi2lab*  
*Instrument: [qi2lab DMD-SIM](https://opg.optica.org/boe/fulltext.cfm?uri=boe-12-6-3700&id=451508).*

### Example 2. Reconstruction parameters: Resolution target 2D-SIM

![Clipboard-1](https://user-images.githubusercontent.com/26783318/166563449-ee752ecd-fd03-47a3-be4c-ea37910aef68.png)

*Sample: Argolight SIM slide v1*  
*Imaged by: Dr. Peter Brown at qi2lab*  
*Instrument: [qi2lab DMD-SIM](https://opg.optica.org/boe/fulltext.cfm?uri=boe-12-6-3700&id=451508).*

### Example 3. Optical sectioning: Tetrahymena immunofluorescence 2D-SIM z stack

![tet_sim_v2](https://user-images.githubusercontent.com/26783318/166837008-e2c718b8-36e4-4efa-b9ee-59593ebdd835.gif)

*Sample: Fixed Tetrahymena, 1-color immunofluorescence for basal bodies.*  
*Prepared by Dr. Nick Galati at [Western Washington University](https://wp.wwu.edu/galatilab/).*  
*Imaged by: Dr. Peter Brown at qi2lab.*  
*Instrument: [qi2lab DMD-SIM](https://opg.optica.org/boe/fulltext.cfm?uri=boe-12-6-3700&id=451508).*

### Example 4. Uncalibrated modulators: Nikon N-SIM three color immunofluorescence 2D-SIM image

![Comparison-1](https://user-images.githubusercontent.com/26783318/166563379-19bc1766-814b-4e55-9add-f7dbd5ceab61.png)

*Sample: Fixed COS cells, 3-color immunofluorescence.*  
*Prepared by: Dr. Christophe Leterrier at [NeuroCyto Lab](https://www.neurocytolab.org/).*  
*Imaged by: Dr. Christophe Leterrier at [NeuroCyto Lab](https://www.neurocytolab.org/).*  
*Instrument: Nikon N-SIM.*

### Example 5. Uncalibrated modulators: Oblique plane structured illumination microscopy (no video walkthrough)

![opsim-1](https://user-images.githubusercontent.com/26783318/170584109-9b59543d-57c8-456e-b5b8-0d8852184000.png)

*Sample: Cardiomyocyte cells, 1-color immunofluorescence for alpha-actinin-2.*  
*Prepared by: James Hayes and Dr. Dylan Burnette at [Vanderbilt University](https://lab.vanderbilt.edu/dylan-burnette-lab/).*  
*Imaged by: Dr. Reto Fiolka at [University of Texas Southwestern Medical Center](https://www.utsouthwestern.edu/labs/fiolka/).*  
*Instrument: [Fiolka lab oblique plane structured illumination microscope](https://www.biorxiv.org/content/10.1101/2022.05.19.492671v1.full).*
