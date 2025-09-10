# wind-data-example

Minimal, public-safe example showing how I manage, compile and visualise data in Python.
The script creates a **toy** weather grid (u,v winds), interpolates to turbine positions
using a KDTree with inverse-distance weights, simulates power via a tabular power curve,
aggregates to “park” level, computes RMSE/MAE versus synthetic “observations”, and saves CSVs.

## What this demonstrates
- Data loading/creation, cleaning and alignment (pandas/xarray)
- Spatial interpolation with KDTree (scipy)
- Simple power-curve based simulation (numpy)
- Aggregation & metrics (pandas, scikit-learn)
- Visualisation (matplotlib)

## Run locally
```bash
python -m venv .venv && . .venv/bin/activate  # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
python wind_data_example.py
