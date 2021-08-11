# LMA 2021 Bioimage analysis in Python workshop

Repository for the Bioimage Analysis in Python tutorial at LMA 2021

In this tutorial, we will explore some of the most critical Python libraries for scientific computing on images, by walking through fundamental bioimage analysis applications of linear filtering (aka convolutions), segmentation, and object measurement, leveraging the napari viewer for interactive visualisation and processing. We will also demonstrate how to extend these concepts to bigger-than-RAM images using Dask.

The target audience are people aiming to work with images and doing image visualization and analysis. Intermediate Python experience (comfortable with python functions, classes, and running code in jupyter notebooks), experience with the scientific Python ecosystem (e.g. NumPy and SciPy) are desired tutorial prerequisites.

## Installation

We recommend that you use Python 3.9 for this tutorial. Both 3.7 and 3.8 should also work but have not been tested. If you are using macOS Big Sur, only Python 3.9 works.

To perform this tutorial, we first need to set up our environment. To do so, please copy the repository containing the tutorial materials to your computer. We recommend cloning the materials into your Documents folder, but you can choose another suitable location.

### Method 1: using git

If you already use git, follow these instructions to clone the repo to your local computer. You may want to change the folder to which you clone the repo.

```bash
cd ~/Documents
```

and then clone the repository. This will download all of the files necessary for this tutorial.

```bash
git clone https://github.com/jni/lma-2021-bioimage-analysis-python
```

Then, navigate to the directory you just cloned.

```bash
cd lma-2021-bioimage-analysis-python
```

### Method 2: Download a zip file

If you don't want to use git, you can download a zip file from the repo:

![download link screenshot](images/repo-screenshot.png)

Unzip the files to a folder of your choice.

### Setting up an environment

Next we must install the dependencies for this tutorial, which can be done either with conda or pip.

#### with conda

We have provided a conda environment file to set up your python environment for this tutorial. To install the dependencies, please enter the following. This may take 5-10 minutes.

Use:

```
conda env create -f environment.yml
```

Follow the instructions for installation. When the installation completes successfully, you should see the following

```bash
done
#
# To activate this environment, use
#
#     $ conda activate lma21
#
# To deactivate an active environment, use
#
#     $ conda deactivate
```

Once the installation has been completed, activate your tutorial environment

```bash
conda activate lma21
```

#### with pip

Alternatively, in an environment including pip, use:

```
pip install -U -r requirements.txt
```

### checking your installation

You can test to make sure napari was installed correctly launching napari from the command line using the command below.

```bash
napari --info
```

You are now ready to start the tutorial! We will perform the analysis using Jupyter Notebook. To start Jupyter Notebook, enter

```bash
jupyter notebook
```

Jupyter Notebook will open in a browser window and if you click on the lectures folder you'll be ready to get started!


## Datasets

For the dask tutorial, we are going to be using some 3D + t datasets from the
[Cell Tracking Challenge](http://celltrackingchallenge.net/3d-datasets/),
specifically:

- the [C. elegans developing embryo training
  dataset](http://data.celltrackingchallenge.net/training-datasets/Fluo-N3DH-CE.zip)
  (3GB), **OR**, if that is too large for you to comfortably download,
- the [Chinese Hamster Ovarian (CHO) nuclei overexpressing GFP-PCNA training
  dataset](http://data.celltrackingchallenge.net/training-datasets/Fluo-N3DH-CHO.zip)
  (98MB)


## Getting help after the workshop

There are several forums you can use to get help and advice with your image analysis after this workshop is over.

* The image.sc forum is an excellent general source of advice, either by searching old questions or adding your own: https://forum.image.sc
* For questions specifically about napari, you can post in the napari zulip chat: https://napari.zulipchat.com

## Further learning resources

As suggested by workshop participants

* The BioImage Informatics Index training materials page - https://biii.eu/training-material
* The freely available textbook *"Bioimage data analysis workflows"* by Kota Miura and Nataša Sladoje. The complete book can be downloaded in full (epub/pdf) from several locations on the web, [including here](https://link.springer.com/book/10.1007/978-3-030-22386-1).
* NEUBIAS training materials
    * The [NEUBIAS YouTube channel](https://www.youtube.com/c/NEUBIAS/videos)
    * The [NEUBIAS Academy @ Home webinars](http://eubias.org/NEUBIAS/training-schools/neubias-academy-home/)
* Tutorial materials on [Interactive Bioimage Analysis with Python and Jupyter](https://github.com/guiwitz/neubias_academy_biapy) by Guillaume Witz
* This [list of annotation tools for machine learning research](https://www.simonwenkel.com/2019/07/19/list-of-annotation-tools-for-machine-learning-research.html)
* ... and many other suggestions compiled in [this forum discussion](https://forum.image.sc/t/bioimage-analysis-recommended-reading-and-viewing/28051) (there's a ton of information and suggestions in that discussion thread!)
