# AI


This repository serves as a collection of walkthroughs, utilities, and other resources to improve the NREL AI/ML user's quality of life, both novice and expert.

The tutorial notebooks can be run using a local installation of Juypter notebooks, or they can be run using Google Colab which does not use local resources and will typically result in faster training times. Google Colab also has many of the ML prerequisites installed.

If you would like to run the tutorials using a local Python notebook application such as Jupyter notebooks, you can do so easily by installing a Conda environment using the included `environment.yml` file. The steps to do so are as follows:

1. Ensure you have a working Conda distribution.
2. Create a new conda environment using the environment file: `conda env create --file environment.yml`.
3. Activate the new environment: `conda activate nrel-ai`.
4. Launch jupyter-lab in terminal with `jupyter-lab` and navigate to the desired tutorial.

Once you have a working conda environment you can keep it up-to-date if there have been any changes to the `environment.yml` file with: `conda env update --name nrel-ai --file environment.yml --prune`


## Supervised



