# Landholder Dominance and Moisture Flows

## Overview

The Amazon rainforest helps regulate South America's water cycle, but the influence of land-use decisions on moisture flows and regional rainfall is not fully understood. This project supports research into how dominant landholder groups shape rainfall across South America and the resilience of the Amazon rainforest. The study combines high-resolution land-use/land-cover data with moisture-tracking model outputs to examine where rainfall linked to different landholder groups falls, including over forests, croplands, and pastures. It also considers how deforestation and other land conversions may affect these moisture connections, regional rainfall, agricultural production, and ecosystem resilience.

The code accompanies the paper [“Landholders leverage over rainfall and resilience of Amazon rainforest”](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6814007) (SSRN abstract 6814007).

## Research workflow

The project's analysis areas include:

1. **Landholder dominance:** Prepare spatial landholder-dominance analyses using MapBiomas and HILDA+ land-cover products.
2. **Property data:** Analyze SICAR property data and compare landholder classifications.
3. **Moisture recycling:** Estimate moisture recycling using MapBiomas- and HILDA+-based land-use inputs.
4. **Resilience:** Assess rainfall and ecosystem-resilience scenarios over the Amazon study area.
5. **Moisture footprints:** Summarize and visualize moisture footprints, including volumetric results.

**Manuscript versions:** Version labels refer to manuscript versions: v1 is the first version and v2 is the second, not software or model releases.

These are descriptions of the project's analysis areas, not runnable instructions: the current `main` branch contains this README only; the analysis notebooks and other project files are not currently included.

## Data and reproducibility

Input datasets are not hosted in this repository. The analyses have used or referenced land-cover products such as MapBiomas and HILDA+, SICAR property data, South American administrative boundaries, raster grids, and climate and moisture datasets. Obtain data from their original providers and confirm each dataset's source, time period, resolution, coordinate reference system, and terms of use before analysis.

The prior notebooks referenced machine-specific file paths and did not provide a pinned software environment or complete data manifest. As the notebooks are not currently present, this repository does not provide a runnable setup or tested reproduction procedure.

## System requirements

The analysis notebooks use the following Python packages: NumPy, pandas, xarray, rioxarray, rasterio, GeoPandas, Fiona, Shapely, geocube, Matplotlib, Cartopy, tqdm, scikit-learn, statsmodels, skextremes, Plotly, and seaborn. Compatible versions may be required; this repository does not provide a pinned dependency file. Requirements also depend on the input data and geospatial libraries available for your platform.

## Repository contents

- `README.md` — project overview and data/reproducibility notes.

## License

No license file is currently included in this repository. The terms for reuse of the project materials are therefore not specified here. Input datasets may have separate licenses and usage restrictions; consult their original providers.
