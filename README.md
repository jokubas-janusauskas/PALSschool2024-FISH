# Transcriptomics2024-FISH
#### Before we proceed, I recommend you make a folder dedicated to today's workshop and download all the files in this repository to it.
## Install MiniConda
#### We'll be running some Python scripts. For that we'll need Conda. Follow the instructions here to install it from command line on your OS:
#### https://docs.anaconda.com/miniconda/#quick-command-line-install
## Set up the Conda environment
#### Once Conda is installed, we'll need to set up the environment. In the terminal, go to the folder with the downloaded files using the command
```console
cd path/to/the/folder
```
#### and execute the following command:
```console
conda env create --name fish_training --file fish_training.yml
```
#### This may take a few minutes
## Activate the environment
#### Activate the environment with the following command:
```console
conda activate
```
## Launching the notebook
#### Add the environment to Jupyter with the following command (only needs to be done once):
```console
python -m ipykernel install --user --name fish_training --display-name "FISH_training"
```
#### Now we're ready to launch the notebook. Execute this command:
```console
jupyter lab
```
#### and open FISH_Training.ipynb file.
