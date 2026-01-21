### 1. Overview
This repository contains codes of an activa learning workflow for exploring the polymorph control of FeC2O4·2H2O in the co-precipitation synthesis. It can be extended to other synthesis systems involving additional synthesis variables such as pH, temperature, or additives, while practical implementation may require upgrading the robotic synthesis system and codes.


### 2. Required Dependencies
Python 3.11  
Numpy 1.26.4  
Pandas 2.2.3  
Scikit-learn 1.2.2  
Torch 2.7.1  
Torchbnn 1.2  
Matplotlib 3.10.3  
Seaborn 0.13.2  
Jupyter 1.1.1  
notebook 7.3.3  


### 3. Installation & Setup 
Clone the repository
```bash
git clone https://github.com/TongZhao-1106/Phase-control-of-Fe2C2O4-2H2O.git
```

Create and activate a virtual environment
```bash
conda create -n your_env python=3.11
```

Activate the environment
```bash
conda activate your_env
```

Install dependencies
```bash
pip install -r requirements.txt
```


### 4. Usage

The active learning loop is implemented as a series of notebooks:
| Notebook | Description |
|----------|-------------|
| GPR_BO.ipynb | Bayesian optimization using Gaussian Process Regression to find the best synthesis conditions of alpha phase |
| RF_AL_iter0.ipynb | Train initial RF model & propose experiments for Iteration 1 |
| RF_AL_iter1.ipynb | Retrain model with updated dataset & propose Iteration 2 experiments |
| RF_AL_iter2.ipynb | Retrain model with updated dataset & propose Iteration 3 experiments |
| RF_AL_iter3.ipynb | Retrain model with updated dataset & test prediction accurancy using randomly selected samples |
| BNN.ipynb / KNN.ipynb / SVM.ipynb / LR.ipynb| Baseline model comparisons without data scaling|
| BNN-scale.ipynb / KNN-scale.ipynb / SVM-scale.ipynb / LR-scale.ipynb | Baseline model comparisons with data scaling|

All data used for active learning are in the xlsx file. After each active-learning iteration, experimental measurements should be added to the data sheet.
| Data | Description |
|----------|-------------|
| results.xlsx | All synthesis parameters and phase information in this study |	 

Run notebooks:
```bash
jupyter notebook your_file.ipynb
```


