# Reproducibility Package for "Quasi-average predictions and regression to the trend: an application to the M6 financial forecasting competition"

This repository contains the data and code necessary to reproduce the results presented in the paper "Quasi-average predictions and regression to the trend: an application to the M6 financial forecasting competition" by Jose M. G. Vilar. The article has been submitted to the International Journal of Forecasting and is available as a preprint at https://arxiv.org/abs/2410.08009.

## Repository Information

- **Date**: December 12, 2024
- **Author**: Jose M. G. Vilar (j.vilar@ikerbasque.org)
- **Affiliations**: 
  1. Biofisika Institute (CSIC, UPV/EHU), University of the Basque Country (UPV/EHU)
  2. IKERBASQUE, Basque Foundation for Science

## Repository Structure

```
M6competition/
├── code/
│   └── m6paper.ipynb
├── data/
│   ├── AdjClose.csv.gz
│   └── M6_Universe.csv
└── output/
    ├── fig1.[eps,pdf,png,svg]
    ├── fig2.[eps,pdf,png,svg]
    ├── fig3.[eps,pdf,png,svg]
    ├── fig4.[eps,pdf,png,svg]
    └── fig5.[eps,pdf,png,svg]
```

## Computing Environment

### Computing Environment

- Operating System: Debian GNU/Linux 12
- Conda Version: 24.11.0
- Python Version: 3.12.7 (conda-forge)

### Required Python Packages
- pandas 2.2.2
- numpy 2.0.2
- matplotlib 3.9.2
- notebook 7.2.2

### Installation
```bash
# Create and activate conda environment
conda create -n m6paper python=3.12.7
conda activate m6paper

# Install required packages
conda install -c conda-forge pandas=2.2.2 numpy=2.0.2 matplotlib=3.9.2 notebook=7.2.2
```

## Data Description

The repository includes the following datasets:

- `AdjClose.csv.gz`: Compressed CSV file containing adjusted closing prices, downloaded from Yahoo Finance
- `M6_Universe.csv`: List of assets in the M6 competition universe, provided by the competition organizers



## Running the Code

1. Clone the repository:
```bash
git clone https://github.com/jmgvilar/M6competition.git
cd M6competition
```

2. Execute the Jupyter notebook:
```bash
jupyter nbconvert --to notebook --execute --inplace code/m6paper.ipynb
```

The notebook will generate five figures (Fig. 1-5) in multiple formats (PDF, SVG, PNG, EPS) in the `output` directory.

## Figure Generation

The notebook generates the following figures:
- Fig. 1: Quintile distribution histograms
- Fig. 2: RPS time series plots
- Fig. 3: Return ratio time series
- Fig. 4: Information ratio comparisons
- Fig. 5: Strategy comparison plots

Each figure is saved in multiple formats (PDF, SVG, PNG, EPS) in the `output` directory.

## Additional Results

The data presented in Table 1 of the article was obtained from the M6 competition leaderboard available at https://github.com/Mcompetitions/M6-methods/blob/main/IJF%20paper/summary_leaderboard.xlsx. The data for the article methods corresponds to Team db21f28b 21 in the leaderboard.

## Computing Requirements

- **Memory**: Minimum 8GB RAM recommended
- **Storage**: ~10MB for all data and output files
- **Runtime**: Approximately 5-10 minutes on a standard desktop computer
- **Special Requirements**: None (no GPU or parallel computing needed)

## License

All code is provided under the MIT License.

## Contact

For questions or issues regarding this reproducibility package, please contact:
Jose M. G. Vilar (j.vilar@ikerbasque.org)
