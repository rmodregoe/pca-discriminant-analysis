
# Principal Component and Discriminant Analysis on Human Body Measurements

## Project Description
This project analyzes a dataset of human body measurements to explore relationships among variables and investigate key factors distinguishing males and females. It includes:
- Principal Component Analysis (PCA) to identify patterns and reduce dimensionality.
- Discriminant Analysis to classify and interpret gender-based differences.

## Features
- **Principal Component Analysis (PCA)**:
  - Identifies the primary components explaining variability in body measurements.
  - Visualizes individuals in a reduced dimensional space.
- **Discriminant Analysis**:
  - Constructs discriminant functions for gender classification.
  - Evaluates classification accuracy using confusion matrices and cross-validation.

## Included Files
1. **Code**:
   - `prinfact.R`: Custom R script for PCA computation.
2. **Dataset**:
   - `body.txt`: Contains body measurements of 507 individuals, including skeletal and muscle dimensions, age, weight, height, and gender.

## Dataset Description
The dataset includes the following groups of variables:
1. **Skeletal Measurements**:
   - Shoulder Diameter (`A_hombros`)
   - Pelvic Width (`A_pelvis`), etc.
2. **Muscular Measurements**:
   - Shoulder Circumference (`C_hombros`)
   - Chest Circumference (`C_pecho`), etc.
3. **Other Measurements**:
   - Age (years)
   - Weight (kg)
   - Height (cm)
   - Gender (1 - Male, 0 - Female)

## Requirements
- **R**: Version 4.0 or higher
- Required Libraries:
  - `MASS`
  - `car`

Install the libraries using:
```R
install.packages(c("MASS", "car"))
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/rmodregoe/pca-discriminant-analysis.git
   ```
2. Load the dataset in R:
   ```R
   data <- read.table("body.txt", header = TRUE)
   ```
3. Run PCA:
   ```R
   source("prinfact.R")
   pca_result <- prinfact(data[, 10:21], r = 2)
   ```
4. Perform discriminant analysis using your preferred R functions or custom scripts.

## Results
- PCA results highlight relationships and variability among body measurements.
- Discriminant Analysis provides insights into gender classification and variable importance.

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
Created by Ricardo Modrego. For questions or comments, contact me at [r.modrego.e@gmail.com](mailto:r.modrego.e@gmail.com).
