# Bi625_ML_Assignment

In this assignment, you will gain a familiarity with Machine Learning approaches to analyze two main types of biological data, images and sequences. 

In part 1, you will analyze a dataset from HappyWhale's Kaggle competition (Feel free to check out the original competition here: https://www.kaggle.com/competitions/humpback-whale-identification/overview). You will only analyze a small subset of this dataset that is already on Talapas ready for your use. This dataset possesses individual humpack whales with pictures of their flukes. Your goal is to run and modify a classifier that sorts whale fluke images into whale individuals' "names". 

In part 2, you will analyze a dataset from Gresova et al., 2023. This dataset possesses human sequences from intergenomic and coding regions. Your goal is to run and build a classifier that sorts sequences by their annotation (coding vs intergenomic).


#### Conda environments
```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/HumpbackClassifierEnv``` for the humpback whale classifier
```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/SequenceClassifier``` for the sequence classifier

### Optional: Weights and biases
Weights and biases is a platform that allows researchers to track model perforamnce, collaborate, and build better models faster. After making an account, you can log into weights and biases via the command line then use their commands to track your training progress.

Activate the conda environment (/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/HumpbackClassifierEnv), then type in 
```wandb login``` and paste your API login key.

You can find your weights and biases API key by logging into weights and biases on Chrome and going to the quickstart page.

#### Part 1 Humpback Whale Classifier Jupyter launch:
Account: bgmp; SLURM partition: gpu; Number of hours: 2; CPU Cores: 6; Total Memory: 32; Check box for GPU Enabled; Alternate Conda Environment: ```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/HumpbackClassifierEnv```

#### Part 2 Sequence Classifier Jupyter launch:
Account: bgmp; SLURM partition: gpu; Number of hours: 2; CPU Cores: 6; Total Memory: 32; Check box for GPU Enabled; Alternate Conda Environment: ```/projects/bgmp/shared/Bi625/ML_Assignment/Conda_Envs/SequenceClassifier```

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

