# Bi625_ML_Assignment

In this assignment, you will gain a familiarity with Machine Learning approaches to analyze two main types of biological data, images and sequences. 

In part 1, you will analyze a dataset from HappyWhale's Kaggle competition. This dataset possesses individual humpack whales with pictures of their flukes. Your goal is to run and modify a classifier that sorts whales by their flukes. 

In part 2, you will analyze a dataset from Gresova et al., 2023. This dataset possesses human sequences from intergenomic and coding regions. Your goal is to run and build a classifier that sorts sequences by their status (coding vs intergenomic).

## Completing this assignment

To run this assignment, you will be using Talapas OnDemand (https://ondemand.talapas.uoregon.edu/) which will allow you to visualize what the model is "seeing" and "doing". Please note, the humpback whale classifier and the sequence classifier use two different machine learning modules (pytorch and tensorflow, respectively). Therefore, you will use one conda environment for the humpback whale classifier and a different conda environment for the sequence classifier. 

### First, clone this repo
Open Talapas via the command line or VS code, and clone this repository into your bgmp directory.

### Optional: Weights and biases
Weights and biases is a platform that allows researchers to track model performance, collaborate, and build better models faster. 

Log into weights and biases after activating the conda environment and paste your API key when prompted
```wandb login```
You can find your weights and biases API key by logging into weights and biases on Chrome and going to the quickstart page.

### Then, launch Talapas OnDemand
Open Talapas OnDemand via Chrome, navigate to Interactive Apps then Jupyter, and finally fill out the Jupyter notebook launch page accordingly. Follow the directions from inside the notebooks to complete the assignmnet. 

#### Part 1 Humpback Whale Classifier Jupyter launch:
Account: bump; SLURM partition: gpu; Number of hours: 2; CPU Cores: 6; Total Memory: 32; Check box for GPU Enabled; Alternate Conda Environment: ```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/HumpbackClassifierEnv```

#### Part 2 Sequence Classifier Jupyter launch:
Account: bump; SLURM partition: gpu; Number of hours: 2; CPU Cores: 6; Total Memory: 32; Check box for GPU Enabled; Alternate Conda Environment: ```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/SequenceClassifier```

### A Final Note:
If you get really into optimizing these ML models, it would be wise to switch from Talapas OnDemand and the Jupyter notebook to using the command line and a python script. In this case, fill out the Jupyter notebooks up until the "code and explore" sections (and submit the pdf of the Jupyter notebook). Then, convert the .ipynb to a python script and make your modifications for the "code and explore" sections. Submit the "code and explore" python script, .out file, and an images that it produced.

### Information on the Conda enviornments
The conda environments for this assignment have been set up for you using the below packages. The packages are listed below for your reference.

#### Humpback Whale 
```
## Do not run the below commands
## The conda environment has already been created
conda install jupyter
conda install conda-forge::scikit-learn
conda install pytorch
conda install captum -c conda-forge
conda install conda-forge::imageio
conda install matplotlib
conda install scipy
conda install tensorboard
conda isntall torchvision
conda install pandas
conda install tqdm
conda install seaborn
pip install wandb
```

#### Sequences 

```
## Again, do not create this conda environment
## It has already been made
conda create -n "Sequences" tensorflow=2.14 keras
pip install tfa-nightly
conda install jupyter
pip install genomic-benchmarks
pip install wandb
