# Downscaling Land Surface Temperature from 100m to 10m Using Landsat & Sentinel-2

This repository demonstrates a workflow to downscale Land Surface Temperature (LST) from 100 m to 10 m spatial resolution by leveraging thermal data from Landsat-8 and multispectral data from Sentinel-2. The approach uses machine learning (XGBoost regression) and Microsoft's Planetary Computer for data access and processing.

**Soon, a detailed methodology and code walkthrough will be available on my [Medium blog](https://medium.com/).**

---

## 🚀 Features

* **High-Resolution LST Estimates**: Improve 100 m thermal observations to 10 m resolution.
* **XGBoost Regression**: Ensemble-based regressor to model the relationship between Sentinel-2 bands and Landsat thermal band.
* **Coregistered Samples**: Select same-date images, sample randomly for robust model training.
* **Planetary Computer Integration**: Access data via STAC API in notebooks.
* **Reproducible Notebooks**: Ready-to-run Jupyter notebooks for exploration, training, and inference.

## 📂 Repository Structure

```
├── Data/                 # Sample CSVs and TIFFs for training & testing
├── NB/                   # Jupyter notebooks (.ipynb) for each step
│   ├── 01_data_preparation.ipynb
│   ├── 02_model_training.ipynb
│   └── 03_inference.ipynb
├── model/                # Trained XGBoost model artifacts (.json/.bin)
├── requirements.txt      # Python dependencies
└── README.md             # This file
```

## 🛠 Prerequisites

* Python 3.8 or higher
* Anaconda or virtualenv
* Install dependencies:

```bash
pip install -r requirements.txt
```

Dependencies include:

* `xarray`, `rasterio`, `geopandas` for geospatial data handling
* `xgboost` for regression modeling
* `pandas`, `numpy` for data manipulation
* `planetary-computer` or `pystac-client` for STAC data access

## 🔧 Usage

1. **Clone the repository**

   ```bash
   ```

git clone [https://github.com/zubair9703/Downscaling\_temp100m\_10m.git](https://github.com/zubair9703/Downscaling_temp100m_10m.git)
cd Downscaling\_temp100m\_10m

```

2. **Explore data preparation**
- Open `NB/01_data_preparation.ipynb`.
- Coregister same-date Landsat-8 & Sentinel-2 tiles.
- Generate random sample points and export to CSV in `Data/`.

3. **Train the model**
- Open `NB/02_model_training.ipynb`.
- Load sample CSVs, train XGBoost regressor.
- Model artifacts saved under `model/`.

4. **Run inference**
- Open `NB/03_inference.ipynb`.
- Apply trained model to Sentinel-2 imagery.
- Output downscaled LST GeoTIFF.

## 📈 Results

_Example visualization of downscaled vs original LST_ (see notebooks for figures)


## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License.

## 📫 Contact

For questions or feedback, reach out to Zubair Ahmed at **zubahme97@gmail.com**.

```
