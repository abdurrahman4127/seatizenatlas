# Seatizen Atlas Dataset

This [notebook](https://github.com/abdurrahman4127/seatizenatlas/blob/main/SeatizenAtlasX) utilizes `aria2`, a download utility to retrieve marine image datasets from Zenodo. The download process is optimized for speed through parallel connections and segmented downloading.

### Download Configuration

The [notebook](https://github.com/abdurrahman4127/seatizenatlas/blob/main/SeatizenAtlasX) employs these key `aria2` parameters:
- `--max-connection-per-server=16`: Establishes up to 16 connections per server
- `--split=32`: Splits each file into 32 segments for parallel downloading
- `--min-split-size=1M`: Ensures segments are at least 1MB in size
- `--max-concurrent-downloads=16`: Allows simultaneous downloading of multiple files
- `--continue=true`: Enables automatic resumption of interrupted downloads

## Segmentation Mask
The dataset contains 14,492 multilabel annotation images. Among them, only ~1,200 images contain detailed instance segmentation masks. We separate the samples having no segmentation mask to the `/content/dataset/unlabelled/` directory. If you work locally or want to download the dataset directly to your Colab environment (note: you can't upload the data to your Google Drive unless you have over 35GB, but you can directly download and use it in your Colab environment), just run the code to see the directory organization. The list of samples w/o the segmentation masks is provided in the [csv](https://github.com/abdurrahman4127/seatizenatlas/blob/main/labeled_image_names.csv) file. 

## Original Source
The dataset is sourced from Zenodo (published on October 18, 2024; *Version 1.1.0*). More information is available in the [Scientific Data publication](https://doi.org/10.1038/s41597-024-04267-z) and on [Zenodo](https://doi.org/10.5281/zenodo.13951614). If you use this dataset, cite the publication and the Zenodo data. 

## Data in Kaggle
The whole dataset (Version 1.1.0) is uploaded to Kaggle. If you prefer to work in Kaggle, see the data at [abdurrahman4127/seatizenatlas](https://www.kaggle.com/datasets/abdurrahman4127/seatizenatlas).
