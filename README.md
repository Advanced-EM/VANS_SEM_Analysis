# VANS SEM Image Analysis

## Overview

This project provides comprehensive morphological analysis of Vertically Aligned Nanostructures (VANS) from SEM plan-view images. The analysis extracts pillar size distributions, shape characteristics, and spatial arrangements with publication-quality visualizations and statistical reports.

## Features

- **Automated Image Processing**: Preprocessing, segmentation, and watershed analysis
- **Comprehensive Feature Extraction**: Size, shape, and spatial characteristics
- **Statistical Analysis**: Distribution analysis, outlier detection, and correlation studies
- **Publication-Quality Outputs**: High-resolution plots and statistical summary tables
- **Data Export**: CSV format for further analysis in statistical software

## Project Structure

```
VANS_SEM_Analysis/
├── README.md                    # This file
├── grain_analysis.ipynb         # Main analysis notebook
├── VANs plan-view.jpg          # Input SEM image
└── analysis_results/           # Generated outputs
    ├── 00_original_with_scale.png
    ├── 01_preprocessing.png
    ├── 02_segmentation.png
    ├── 03_watershed.png
    ├── 04_comprehensive_analysis.png
    ├── 05_advanced_statistics.png
    ├── 06_statistical_summary.png
    ├── 07_spatial_overlay.png
    ├── 08_size_categories_overlay.png
    └── pillar_analysis_data.csv
```

## Requirements

### Python Libraries
- `opencv-python` (cv2)
- `numpy`
- `matplotlib`
- `scikit-image`
- `scipy`
- `pandas`
- `seaborn`

### Installation
```bash
pip install opencv-python numpy matplotlib scikit-image scipy pandas seaborn
```

## Usage

1. **Setup**: Place your SEM image in the project directory
2. **Configure**: Update the `image_path` and `pixels_to_nm_factor` in the notebook
3. **Run Analysis**: Execute all cells in `grain_analysis.ipynb`
4. **Review Results**: Check the `analysis_results/` folder for outputs

### Key Configuration Parameters

- `pixels_to_nm_factor`: Conversion factor from pixels to nanometers (default: 1.0)
- `sigma_blur`: Gaussian blur parameter for noise reduction (default: 1.0)
- `min_size`: Minimum object size for segmentation (default: 30 pixels)

## Analysis Methodology

1. **Image Preprocessing**
   - Grayscale conversion
   - Gaussian filtering for noise reduction
   - Contrast enhancement

2. **Segmentation**
   - Otsu thresholding
   - Morphological cleaning
   - Watershed segmentation for touching objects

3. **Feature Extraction**
   - Equivalent diameter calculation
   - Shape descriptors (circularity, aspect ratio, solidity)
   - Spatial coordinates and distribution

4. **Statistical Analysis**
   - Distribution analysis with KDE fitting
   - Outlier detection and removal
   - Correlation analysis between features
   - Size uniformity assessment

## Output Files

### Visualization Files
- **01_preprocessing.png**: Grayscale conversion and filtering steps
- **02_segmentation.png**: Binary segmentation results
- **03_watershed.png**: Watershed segmentation with object labels
- **04_comprehensive_analysis.png**: Main statistical plots and distributions
- **05_advanced_statistics.png**: Advanced statistical visualizations
- **06_statistical_summary.png**: Publication-ready summary table
- **07_spatial_overlay.png**: Spatial distribution on original image
- **08_size_categories_overlay.png**: Size-categorized pillar distribution

### Data Files
- **pillar_analysis_data.csv**: Complete dataset with all extracted features

## Key Metrics

The analysis provides the following key morphological metrics:

- **Size Distribution**: Mean, standard deviation, and percentiles of pillar diameters
- **Shape Quality**: Circularity and aspect ratio measurements
- **Size Uniformity**: Coefficient of variation assessment
- **Spatial Distribution**: Pillar arrangement and clustering analysis

## Customization

### Segmentation Parameters
Adjust these parameters in the notebook for different image types:
- `sigma_blur`: Increase for noisier images
- `min_size`: Adjust based on expected pillar sizes
- `min_distance` in watershed: Control separation of touching objects

### Statistical Analysis
- Outlier detection: Modify the `factor` parameter in `filter_outliers()`
- Size categories: Adjust thresholds in the spatial distribution analysis

## Citation

If you use this analysis in your research, please cite appropriately and consider sharing improvements back to the community.

## License

This project is provided as-is for research and educational purposes.

## Contact

For questions or improvements, please open an issue or submit a pull request.

## Repository

GitHub: https://github.com/Advanced-EM/VANS_SEM_Analysis