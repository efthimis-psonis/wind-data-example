# Offshore Wind Farm Simulation

This repository contains Python code I developed during my Master’s Thesis at the University of Liège,
focusing on predictive modeling of Belgian offshore wind farms.

The code:
- Loads weather datasets (NetCDF format, e.g. ERA5)
- Interpolates wind conditions from grid points to turbine coordinates using KDTree
- Simulates turbine power output via tabular power curves
- Aggregates production to park level
- Computes metrics (RMSE, MAE, bias) against real production
- Saves turbine- and park-level outputs to CSV

⚠️ Real production and weather datasets are **not included** due to confidentiality.  
The code remains executable if you provide your own datasets in the expected format.

---

## Structure
- `simulation/models.py` – turbine models and specs
- `simulation/interpolate.py` – spatial interpolation
- `simulation/simulate.py` – simulation pipeline
- `simulation/run.py` – yearly batch runs
- `examples/example_run.py` – usage demo with placeholders

## Install
```bash
pip install -r requirements.txt
