# AI for Sustainability – Delhi NCR Airshed Analysis



This project leverages **AI and remote sensing data** to analyze land cover and generate datasets for sustainability research in the **Delhi NCR region**.

---

## 📌 Project Overview

The aim of this project is to build a dataset of satellite images and their corresponding land cover labels to support AI-based sustainability analyses. Using ESA WorldCover data, we identify dominant land cover types (vegetation, cropland, built-up, water, etc.) for each image tile.

Key steps include:

1. **Label Construction & Dataset Preparation**  
   - Filter satellite images.  
   - Map each image to its landcover label using ESA WorldCover 2021 data.

2. **Train-Test Split**  
   - Stratified split of the dataset for ML model training.  

3. **Data Export**  
   - Save full, training, and test datasets as CSV files for downstream AI models.

---

## 🗂 Folder Structure
AI_for_Sustainability/
│
├── Raw_Data/ # Original satellite imagery and geospatial files
│ ├── delhi_airshed.geojson
│ ├── delhi_ncr_region.geojson
│ └── worldcover_bbox_delhi_ncr_2021.tif
  └── RGgb
│
├── Output/ # Generated datasets and filtered images
│ ├── filtered_images.txt
│ ├── dataset.csv
│ ├── train_dataset.csv
│ └── test_dataset.csv
| └── confusion_matrix
| └── plotncr
| └── grid_plot
├── notebooks/ # Jupyter notebooks
│ └── dataset_preparation_label.ipynb
  ├── model_train.ipynb
  └── spaatial_filter.ipynb
├── Readme

## 🛠 Technology Stack

- Python 3.14  
- Libraries: `numpy`, `pandas`, `rasterio`, `pyproj`, `tqdm`, `scikit-learn`  
- GitHub for version control  
- Optionally Git LFS for large files (`.tif` data)


## ⚙️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/Shivamprajapati149/AI_Sustanibilityy.git
cd AI_Sustanibilityy

📊 Output

dataset.csv – Complete dataset of filtered images and labels

train_dataset.csv – Training set

test_dataset.csv – Test set

sample_images.png – Sample images with land cover labels


📈 Model Accuracy

The trained model achieved the following accuracy on the test set:

Test Accuracy: 0.8402994385527136
F1 Score: 0.861906575998896


