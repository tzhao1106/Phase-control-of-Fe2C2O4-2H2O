1. Overview
This repository contains an active-learning framework for iterative material selective synthesis. 

2. Required Dependencies
Python 3.11 
Numpy 1.26.4
Pandas 2.2.3
Scikit-learn 1.2.2
Torch 2.7.1
Torchbnn 1.2
Matplotlib 3.10.3 
Seaborn 0.13.2

3. Installation & Setup 
3.1 Clone the repository
### Clone the repository
```bash
git clone https://github.com/TongZhao-1106/Phase-control-of-Fe2C2O4-2H2O.git
```

3.2 Create and activate a virtual environment
### Create the Conda environment
```bash
conda create -n activelearn python=3.11
```

### Activate the environment
```bash
conda create -n your_env python=3.9
conda activate your_env
```

### Install dependencies
```bash
pip install -r requirements.txt
```


4. Running the Active-Learning Workflow

The active learning loop is implemented as a series of notebooks:
Notebook	Description
GPR_BO.ipynb	Bayesian Optimization workflow for finding α-phase conditions
BNN.ipynb / KNN.ipynb / SVM.ipynb	Baseline model comparisons without data scaling
BNN-scale.ipynb / KNN-scale.ipynb / SVM-scale.ipynb	Baseline model comparisons
RF_AL_iter0.ipynb	Train model on initial data & generate Iteration 1 proposals
RF_AL_iter1.ipynb	Retrain using new experimental data & generate next proposals
RF_AL_iter2.ipynb	Same workflow for next iteration
RF_AL_iter3.ipynb	Same workflow for next iteration

Data	Description
results.xlsx All synthesis parameters and phase information in this study

