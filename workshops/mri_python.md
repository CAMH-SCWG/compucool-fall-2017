---
title: Neuroimaging with Python
layout: workshop
---

# Intro to Neuroimaging Analysis in Python

[**Click here to go the slides**](https://docs.google.com/presentation/d/1qE-T3g4i2c6pF98zqizzHdal_IB-fiUuacxqg_JldnI/edit?usp=sharing)

--------

## Setting up.. You have three options:

### Option 1: Use the SCC jupyter hub with a guest account
1. log into jupyter hub [https://jupyter.camh.ca](https://jupyter.camh.ca) **This link will only within the CAMH network
2. Naviate to `~/nibabel_nilearn_tutorial_2017/notebook` folder and open ss2017_16mripython.ipynb
 + make sure the "Kernel" in the top right is "Python (3.6_nilearn_01)"
 + you can change the from the top Menu **Kernel**->**Change Kernel**

-----------------------------------------------

### Option 2: Use the SCC jupyter hub with your own account:

1. log into jupyter hub [https://jupyter.camh.ca](https://jupyter.camh.ca) **This link will only within the CAMH network**
2. click on **New**->**Terminal** (top right hand side of home)

inside the terminal
```sh
## clone the git repo
git clone https://github.com/edickie/nibabel_nilearn_tutorial_2017.git

## add the python packages to you jupyter env..
mkdir -p .conda/envs
cd .conda/envs
ln -s /imaging/home/workshop/guest1/.conda/envs/3.6_nilearn_01 3.6_nilearn_01
source activate 3.6_nilearn_01
python -m ipykernel install --user --name 3.6_nilearn_01 --display-name "Python (3.6_nilearn_01)"
source deactivate
```
3. Naviate to `~/nibabel_nilearn_tutorial_2017/notebook` folder and open ss2017_16mripython.ipynb
 + make sure the "Kernel" in the top right is "Python (3.6_nilearn_01)"
 + you can change the from the top Menu **Kernel**->**Change Kernel**
 
------------------------------

## Option 3: Work on your own laptop 

**recommended only for those familiar with setting up conda environments**

1. Clone the repo:
```sh
git clone https://github.com/edickie/nibabel_nilearn_tutorial_2017.git
```
2. build a conda environment with nilearn and seaborn in it..
```sh
conda create -n mripython3.6 python=3.6
source activate mripython3.6
conda install scikit-learn
conda install seaborn
pip install nibabel
pip install -U nilearn
conda install docopt
conda install jupyter
```

3. Inside jupyter, naviagte to the notebook and open it:
 + nibabel_nilearn_tutorial_2017/notebook/ss2017_16mripython.ipynb
 + change the paths at the top of the notebook to places that will work in you laptop...
 
------------------------------------------------------------------------------
## Python Packages from today

+ **Nilearn** [webpage](https://nilearn.github.io/index.html)
    + python package for machine learning that make very pretty plots
    + has an extensive set of online tutorials so it's pretty easy to get started
+ **Nipype** [webpage](http://nipype.readthedocs.io/en/latest/)
    + python package for building neuroimaging analysis workflows
    + also has an extensive set of tutorials to follow

## Useful resources

+ Jody Culham fMRI 4 Newbies [http://www.fmri4newbies.com/](http://www.fmri4newbies.com/)
+ Great [Youtube tutorial channel](https://www.youtube.com/watch?v=9ionYVXUQn8)
+ NITRC [https://www.nitrc.org/](https://www.nitrc.org/)
   + an online resource/database of links to everything neuroimaging
+ [Freesurfer wiki](https://surfer.nmr.mgh.harvard.edu/fswiki)
   + an extensive set of tutorials on everything freesurfer)
+ [CIVET](http://www.bic.mni.mcgill.ca/ServicesSoftware/CIVET-2-1-0-Table-of-Contents)
+ [MAGeT Brain](https://github.com/CobraLab/MAGeTbrain)
+ The FSL wiki
     + [TBSS user guide](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/TBSS/UserGuide)
     + [FSL's randomise tutorial](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Randomise)          
+ Connectome Workbench [tutorial](http://www.humanconnectome.org/documentation/tutorials/)
+ ciftify [github repo](https://github.com/edickie/ciftify)
    + tools written by Erin W Dickie (me!) to make working on the surface (cifti files) easier
+ epitome [github repo](https://github.com/josephdviviano/epitome)
    + a tool written to help you build bash pipelines for fMRI anaylsis
