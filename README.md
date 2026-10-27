PREDICTION OF CARBON AMOUNT IN CATALYTIC METHANE PYROLYSIS

This repository contains a notebook that analyses carbon deposition data and compares three neural network approaches:

- Classic-FNN: feed-forward neural network baseline.

- PINN-M1: Physics-informed model using the notebook's Arrhenius/power-law formulation.

- PINN-M2: Physics-informed model using the notebook's carbon-formation-rate constraint.


REPOSITORY FILES

- `MASS__OF__CARBON__DEPOSITION__CODE.ipynb` — notebook containing data analysis, architecture search, model training and evaluation, and comparison plots.

- `Carbon___Mass___Deposition___Data.csv` — dataset read by the notebook.

- `README.md` — Project description and run instructions.

DATASET

The notebook uses the following input columns.

`T_C`, `Fo_CH4_m3_per_h`, `X_CH4_conv_pct`, `P_input_W`, `TOS_h`

The target columns were `M_C_kg` (carbon mass) and `CFR_kg_per_h` (carbon formation rate). The notebook converted these targets to grams and grams per hour.

Rows missing any of the listed inputs or either target were removed before model fitting.

RUN IN GOOGLE COLAB

1. Open `MASS__OF__CARBON__DEPOSITION__CODE.ipynb’ file in Google Colab.

2. Upload `Carbon___Mass___Deposition___Data.csv` to `/content/`.

3. Run the notebook cells in the existing order.

4. To use the Palatia font in plots, upload an authorized `Palatia.ttf` file to `/content/`. Otherwise, Matplotlib uses its default font.

The notebook uses NumPy, Pandas, PyTorch, scikit-learn, and Matplotlib. Install any missing packages if the runtime reports an import error occurs.

REPRODUCIBILITY

The notebook sets Python, NumPy, and PyTorch random seeds to `42` and configures the cuDNN deterministic settings. Exact reproducibility may still depend on the software version and hardware.

ABOUT THIS CODE

The code was cleaned for presentation and navigation. Markdown title and section-heading cells were added, and the original code cell source and saved outputs were retained. 




