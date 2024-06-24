# EEL-FISH workshop
#### The workshop assumes some familiarity with coding, but simply following the instructions below should get you up and running even if you don't have much experience.
#### If something does not work or if you are struggling with the set up - do not worry, I will be happy to help during the Summer School.

#### Before we proceed any further, I recommend you make a folder dedicated to today's workshop and download FISH_Training.ipynb and fish_training.yml files from this repository to your folder.

#### We'll be using Jupyter notebook in Python for [FISHscale](https://github.com/linnarsson-lab/FISHscale). For that we need to set up a few things (it shouldn't take more than 15 minutes):
## Install MiniConda
#### Conda is the main tool for managing Python packages, environments, etc. If you don't have it yet, follow the instructions [here](https://docs.anaconda.com/miniconda/#quick-command-line-install) to install it from command line for your OS.
#### (N.B. observe that you might need to copy a different download link, according to your OS architecture (as explained in the website)!)

#### If you prefer, there is also a [graphical installer](https://docs.anaconda.com/miniconda/miniconda-install/).

## Set up the Conda environment
#### Once Conda is installed, we'll need to set up an environment with all the required packages. In the terminal, go to the folder that you have created for this workshop by using the command (replace 'path/to/the/folder' with your actual path):
```console
cd path/to/the/folder
```
#### Next, execute the following command to build the Conda environment:
```console
conda env create --name fish_training --file fish_training.yml
```
#### Now let's activate the environment with the following command:
```console
conda activate fish_training
```
#### Finally, download and install the last couple of packages that have to be set up manually (this may take a few minutes):
```console
git clone https://github.com/linnarsson-lab/FISHscale.git
git clone https://github.com/linnarsson-lab/FISHscale.git
cd FISHscale
pip install -e .
cd ../BoneFight
pip install -e .
cd ../

```
#### (You can read more about these packages here: [FISHscale](https://github.com/linnarsson-lab/FISHscale) and [BoneFight](https://github.com/linnarsson-lab/BoneFight))

## Launching the notebook
#### Lastly, we just need to add the environment to our Jupyter with the following command:
```console
python -m ipykernel install --user --name fish_training --display-name "FISH_training"
```
#### And now we're ready to launch the notebook. Execute this command:
```console
jupyter lab
```
#### Once connected, open the FISH_Training.ipynb file. If prompted to select a kernel, choose "FISH_training".
#### After going through this initial set up once, you will only need to activate the environment and launch the notebook if you want to run it again in the future:
```console
conda activate fish_training
jupyter lab

```
#### Feel free to play around and go through the notebook on your own!

## Possible errors
#### Notably, because of some recent OS architecture incompatibilities, unfortunately, you may experience issues when launching the FISHscale interactive visualizer (depending on what machine you are using).
#### If that is the case, you can run:
```console
pip uninstall open3d
```
#### and build the open3d package from [source](http://www.open3d.org/docs/release/compilation.html).
#### However, you should only do this if the interactive visualizer does not work and you do wish to get it working - the rest of the code will run just fine, even if the visualizer does not open.
