# Transcriptomics2024-FISH
#### Today's exercises are based on FISHscale tutorials from the Linnarsson Lab GitHub page:
#### https://github.com/linnarsson-lab/FISHscale
#### (check them out for more use-case examples)
#### Before we proceed, I recommend you make a folder dedicated to today's workshop and download FISH_Training.ipynb and fish_training.yml files from this repository to your folder.
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
#### (this may take a couple of minutes...)

## Activate the environment
#### Now let's activate the environment with the following command:
```console
conda activate fish_training
```
#### And execute the following commands to finish setting it up:
```console
git clone https://github.com/linnarsson-lab/FISHscale.git
cd FISHscale
pip install -e .
cd ../
git clone https://github.com/linnarsson-lab/BoneFight
cd BoneFight
pip install -e .
cd ../
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
#### After the initial set up, you will only need to activate the environment and launch the notebook with the command above!
