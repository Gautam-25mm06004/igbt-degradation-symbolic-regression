# Symbolic Regression of IGBT Degradation (NASA PCoE Accelerated Aging)

Work in progress. Extracts physics-based health indicators (on-state collector-emitter voltage, turn-off overshoot peak and area) from NASA Ames PCoE IGBT accelerated-aging transients and searches for a compact degradation law with PySR, evaluated with chronological splits, multi-seed stability checks, parametric and ML baselines, and RUL metrics.

## Contents

| File | What it does |
|---|---|
| `notebooks/igbt_pysr_degradation.ipynb` | Symbolic Regression of IGBT Degradation (NASA PCoE Accelerated-Aging Data) |

Notebooks are saved with the outputs of their last run, so results and figures can be read on GitHub without running anything.

## Data

NASA Ames Prognostics Center of Excellence, IGBT Accelerated Aging data set (Celaya, Wysocki & Goebel, 2009). The notebook downloads and SHA-256-checks it.

## How to run

The notebooks were developed on Google Colab. Upload a notebook to Colab (File → Upload notebook) and run the cells in order; the first cells install anything missing. To run locally in VS Code instead: `python -m venv .venv`, activate it, `pip install -r requirements.txt jupyter`, then open the notebook and pick the `.venv` kernel. Cells that mount Google Drive (`google.colab`) can be skipped locally if the data files are placed next to the notebook.

Python packages used: `ipython`, `matplotlib`, `numpy`, `pandas`, `pysr`, `scikit-learn`, `scipy`, `sympy` (see `requirements.txt`).

## License

MIT, see `LICENSE`.
