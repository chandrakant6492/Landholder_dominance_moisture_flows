# Landholder dominance and moisture flows

A notebook-based research project investigating how landholder groups and land use in the Amazon influence moisture recycling, regional rainfall, and ecosystem resilience. The notebooks combine land-cover and property data with geospatial and climate inputs to map landholder dominance, estimate moisture connections, and assess resilience scenarios.

> **Data and reproducibility note:** This repository contains analysis notebooks, not the input datasets. The notebooks currently refer to machine-specific paths (for example, `/home/chandra/data/Paper4/`) and do not include a pinned environment or a complete data manifest. Update the input and output paths for your environment and obtain each dataset from its original provider before running the analyses.

## Repository contents

| Notebook | Purpose |
| --- | --- |
| [`1. Data analysis_v3-(HilDA+).ipynb`](<./1.%20Data%20analysis_v3-(HilDA%2B).ipynb>) | Prepare landholder-dominance analyses using HILDA+ land-cover data; exports include NetCDF grids and shapefiles. |
| [`1. Data analysis_v3-(Mapbiomas)_new.ipynb`](<./1.%20Data%20analysis_v3-(Mapbiomas)_new.ipynb>) | Prepare the corresponding MapBiomas-based landholder-dominance analysis. |
| [`1. Data analysis_v3-(Mapbiomas)-Copy1.ipynb`](<./1.%20Data%20analysis_v3-(Mapbiomas)-Copy1.ipynb>) | An additional MapBiomas analysis notebook. Review it alongside the `_new` version to determine which reflects your intended workflow. |
| [`1.1 SICAR_analysis.ipynb`](<./1.1%20SICAR_analysis.ipynb>) | Analyze SICAR property data and compare landholder classifications. |
| [`3.1 Moisture recycling_MapBiomas.ipynb`](<./3.1%20Moisture%20recycling_MapBiomas.ipynb>) and [`3.1 Moisture recycling_MapBiomas-v2.ipynb`](<./3.1%20Moisture%20recycling_MapBiomas-v2.ipynb>) | Estimate moisture recycling with MapBiomas land-use inputs (the repository includes two versions). |
| [`3.2 Moisture recycling_HILDA+.ipynb`](<./3.2%20Moisture%20recycling_HILDA%2B.ipynb>) | Estimate moisture recycling with HILDA+ land-use inputs. |
| [`4. Resilience assessment.ipynb`](<./4.%20Resilience%20assessment.ipynb>) and [`4. Resilience assessment-v2.ipynb`](<./4.%20Resilience%20assessment-v2.ipynb>) | Assess rainfall/resilience scenarios; the notebooks expect gridded data with latitude from -90 to 90 and longitude from 0 to 360, and clip to the Amazon study extent. |
| [`5. Moisture_footprint.ipynb`](<./5.%20Moisture_footprint.ipynb>) and [`5.1 Moisture_footprint (km3 per year).ipynb`](<./5.1%20Moisture_footprint%20(km3%20per%20year).ipynb>) | Summarize and visualize moisture footprints, including volumetric results. |

## Data

Input files are expected to be supplied separately. The notebooks reference land-cover products (including MapBiomas and HILDA+), SICAR property data, South American administrative boundaries, raster grids, and climate/moisture datasets. Confirm the exact source, time period, resolution, coordinate reference system, and usage terms for every dataset used in an analysis; these details are not fully catalogued in this repository.

Generated files are written to paths configured inside the notebooks, including NetCDF grids, shapefiles, figures, and moisture-recycling outputs. The notebooks use local directories under `/home/chandra/data/Paper4/Output/` in several cells. Create your chosen output directories before running cells that write files.

## Getting started

1. Clone the repository and create a Python environment with JupyterLab and the packages used by the notebooks. The notebooks import NumPy, pandas, xarray, rioxarray, rasterio, GeoPandas, Fiona, Shapely, geocube, Matplotlib, Cartopy, tqdm, scikit-learn, statsmodels, skextremes, Plotly, and seaborn. Install compatible versions for your platform; this repository does not currently pin package versions.
2. Obtain the required input datasets from their original providers and place them in your data workspace.
3. Open the notebook you intend to run:

   ```bash
   jupyter lab
   ```

4. Update hard-coded input and output paths in the notebook. Check that the input layers use compatible coordinate reference systems, grid definitions, and coordinate conventions before running analysis cells.
5. Run the notebook cells in order, then inspect the generated maps, tables, and data files. Some analyses are computationally intensive and use multiprocessing.

The notebooks include legacy raster-loading calls such as `xarray.open_rasterio`; depending on your installed package versions, you may need to adapt these calls to the current raster I/O APIs. Because no tested dependency lockfile is provided, exact environment setup may require adjustment.

## License

The project code is provided under the [MIT License](LICENSE). Input datasets may have separate terms; consult their original providers before reuse or redistribution.
