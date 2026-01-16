### 1. Overview
This repository contains an active-learning framework for iterative material selective synthesis. 


### 2. Required Dependencies
Python 3.11 
Numpy 1.26.4
Pandas 2.2.3
Scikit-learn 1.2.2
Torch 2.7.1
Torchbnn 1.2
Matplotlib 3.10.3 
Seaborn 0.13.2
Jupyterlab 4.3.7


### 3. Installation & Setup 
Clone the repository
```bash
git clone https://github.com/TongZhao-1106/Phase-control-of-Fe2C2O4-2H2O.git
```

Create and activate a virtual environment
```bash
conda create -n activelearn python=3.11
```

Activate the environment
```bash
conda create -n your_env python=3.9
conda activate your_env
```

Install dependencies
```bash
pip install -r requirements.txt
```


### 4. Running the Active-Learning Workflow

The active learning loop is implemented as a series of notebooks:
| Notebook | Description |
|----------|-------------|
| GPR_BO.ipynb | Bayesian optimization using Gaussian Process Regression |
| RF_AL_iter0.ipynb | Train initial RF model & propose experiments for Iteration 1 |
| RF_AL_iter1.ipynb | Retrain model with new data & propose Iteration 2 experiments |
| RF_AL_iter2.ipynb | Continue active-learning loop with updated data |
| RF_AL_iter3.ipynb | Final AL iteration for demonstration |
| BNN.ipynb / KNN.ipynb / SVM.ipynb / LR.ipynb| Baseline model comparisons without data scaling|
| BNN-scale.ipynb / KNNBNN-scale.ipynb.ipynb / SVMBNN-scale.ipynb.ipynb / LRBNN-scale.ipynb.ipynb| Baseline model comparisons with data scaling|

All data used for active learning are in a xlsx file
| Data | Description |
|----------|-------------|
| results.xlsx | All synthesis parameters and phase information in this study |	 

Run notebooks:
```bash
cd/d your_file_path
jupyter notebook your_file.ipynb
```
