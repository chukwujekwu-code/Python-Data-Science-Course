# Python for Data Analysis & Data Science

A comprehensive 13-module course covering Python fundamentals through machine learning, designed for beginners transitioning into data roles.

## Course Modules

| Module | Topic | Description |
|--------|-------|-------------|
| 01 | Python Fundamentals | Variables, data types, operators, strings |
| 02 | Data Structures | Lists, tuples, dictionaries, sets |
| 03 | Control Flow | Conditionals, loops, comprehensions, exceptions |
| 04 | Functions | Functions, lambda, scope, decorators |
| 05 | File Handling | Text, CSV, JSON files, context managers |
| 06 | NumPy Fundamentals | Arrays, indexing, broadcasting, statistics |
| 07 | Pandas for Data Analysis | DataFrames, filtering, groupby, merging |
| 08 | Data Visualization | Matplotlib, Seaborn, various plot types |
| 09 | Exploratory Data Analysis | EDA workflow, univariate/bivariate analysis |
| 10 | Data Cleaning & Preprocessing | Missing values, outliers, encoding, pipelines |
| 11 | Statistics for Data Science | Descriptive stats, probability, hypothesis testing |
| 12 | Introduction to Machine Learning | Regression, classification, model evaluation |
| 13 | Capstone Projects | Sales analysis, segmentation, predictive modeling |

## Prerequisites

- Python 3.10 or higher
- [uv](https://github.com/astral-sh/uv) package manager

## Setup Instructions

### 1. Install uv

If you don't have uv installed, install it first:

```bash
# On macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or with pip
pip install uv
```

### 2. Clone/Navigate to the Project

```bash
cd python-tutorials
```

### 3. Create Virtual Environment and Install Dependencies

```bash
# Create venv and install all dependencies in one command
uv sync
```

This will:
- Create a `.venv` virtual environment
- Install all required packages (numpy, pandas, matplotlib, seaborn, scipy, scikit-learn, jupyter, ipykernel)

### 4. Register the Jupyter Kernel

After creating the environment, register it as a Jupyter kernel:

```bash
# Activate the virtual environment first
source .venv/bin/activate  # On macOS/Linux
# OR
.venv\Scripts\activate     # On Windows

# Register the kernel
python -m ipykernel install --user --name=python-data-science --display-name="Python (Data Science Course)"
```

### 5. Start Jupyter

```bash
# Option 1: Jupyter Notebook
uv run jupyter notebook

# Option 2: Jupyter Lab
uv run jupyter lab

# option 3: Vscode
In VS Code you typically need to reload the window for it to detect new kernels
Reload Window: Press Ctrl+Shift+P (or Cmd+Shift+P on Mac), type "Reload Window" and select it
```

Then navigate to the `notebooks/` folder and open any module to begin.

## Quick Start (All Commands)

```bash
# One-time setup
uv sync
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
python -m ipykernel install --user --name=python-data-science --display-name="Python (Data Science Course)"

# Start learning
uv run jupyter notebook notebooks/
```

## Project Structure

```
python-tutorials/
├── README.md
├── pyproject.toml
├── .venv/                  # Created by uv sync
└── notebooks/
    ├── 01-python-fundamentals.ipynb
    ├── 02-data-structures.ipynb
    ├── 03-control-flow.ipynb
    ├── 04-functions.ipynb
    ├── 05-file-handling.ipynb
    ├── 06-numpy-fundamentals.ipynb
    ├── 07-pandas-for-data-analysis.ipynb
    ├── 08-data-visualization.ipynb
    ├── 09-exploratory-data-analysis.ipynb
    ├── 10-data-cleaning-and-preprocessing.ipynb
    ├── 11-statistics-for-data-science.ipynb
    ├── 12-introduction-to-machine-learning.ipynb
    ├── 13-capstone-projects.ipynb
    └── assets/
        └── datasets/
            ├── sales_data.csv
            ├── employees.csv
            ├── products.json
            ├── config.json
            ├── server_log.txt
            └── meeting_notes.txt
```

## Selecting the Kernel in Jupyter

When you open a notebook, make sure to select the correct kernel:

1. Click on "Kernel" in the menu bar
2. Select "Change Kernel"
3. Choose "Python (Data Science Course)"

Or if using VS Code:
1. Click on the kernel selector in the top right
2. Select "Python (Data Science Course)"

## Troubleshooting

### Kernel not showing up

If the kernel doesn't appear in Jupyter:

```bash
# List installed kernels
jupyter kernelspec list

# If not listed, reinstall
source .venv/bin/activate
python -m ipykernel install --user --name=python-data-science --display-name="Python (Data Science Course)"
```

### Package import errors

If you get import errors when running notebooks:

```bash
# Make sure you're using the correct kernel
# Reinstall dependencies
uv sync --reinstall
```

### Matplotlib display issues

If plots don't display, ensure you have the magic command at the top of cells:

```python
%matplotlib inline
```

## Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| numpy | >=1.24.0 | Numerical computing |
| pandas | >=2.0.0 | Data manipulation |
| matplotlib | >=3.7.0 | Basic plotting |
| seaborn | >=0.12.0 | Statistical visualization |
| scipy | >=1.10.0 | Scientific computing |
| scikit-learn | >=1.3.0 | Machine learning |
| ipykernel | >=6.25.0 | Jupyter kernel |
| jupyter | >=1.0.0 | Notebook interface |
| notebook | >=7.0.0 | Jupyter Notebook |

## License

MIT License
