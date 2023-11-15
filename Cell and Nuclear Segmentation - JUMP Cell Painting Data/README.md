# Task

Analyze [JUMP Cell Painting Consortium](https://jump-cellpainting.broadinstitute.org/) data.

# Process

### File-naming convention

rXXcXXfXXp01-chXsk1fk1fl1.tiff:
 - rXX: row number of the imaged well
 - cXX: column number of the imaged well
 - fXX: field that was imaged
 - pXX: z-plane
 - chX: fluorescent channels imaged
   - ch1 mitochondria, ch2 actin, golgi, and plasma membrane (AGP), ch3 RNA, ch4 ER, and ch5 nucleus.

### Image sets
Images with the same rXXcXXfXXp01 but different channels (ch1-ch5) represent an image set. Images with the same row and column number (rXXcXX) are from the same well and have been treated with the same chemical compound.

1. Segment nucleus and whole cell in each image set.
2. Perform analysis on segmentation results.

# Results
According to the structure of this repository.

 - data files:
   - all_cells_nuclei.csv: coordinate positions of all nuclei in the image sets.
   - all_cells_features.csv: cell and nucleus information: area, major/minor axis, number, and intensity distribution values (mean, median, percentiles) per channel per cell per well 
 - masks: high contrast images of cellular and nuclear masks from segmentation
 - plots: sample plots from downstream analysis
   - aspect ratio violin plots: cell eccentricity across wells
   - mean intensity boxplots: differential marker expression across wells
   - major axis length, aspect ratio distribution plots: cell size and shape information
   - major axis/minor axis scatter plot across wells: cell eccentricity across wells
   - PCA plots: PCs scatter plot, intensity means correlation with PCs, explained variance
   - mean intensity correlations between markers by well: co-distribution of markers
   - pairgrid pcs intensity plot: correlations between pcs and intensity means, intensity mean distributions by channel
 - segmentation boundaries: cell and nuclear boundaries overlaid on microscopy images
