

---

# Soil Quality Prediction and Fertilizer Recommendation System

## Project Overview
This project uses machine learning to predict soil quality through pH estimation based on RGB values from soil images. By analyzing these images, we can approximate the pH level and then recommend suitable crops and fertilizers, contributing to optimized soil management and sustainable agricultural practices. The main objectives include:
- Extracting RGB values from soil images
- Predicting soil pH values based on RGB input using a Random Forest Regressor model
- Recommending crops based on the pH level
- Suggesting fertilizers based on the soil’s nitrogen (N), phosphorus (P), and potassium (K) requirements

## Features
1. **Soil pH Prediction**: Predicts the pH of the soil based on RGB values using a trained Random Forest model.
2. **NPK Analysis**: Retrieves nitrogen, phosphorus, and potassium levels for different pH levels, helping determine soil nutrient quality.
3. **Fertilizer Recommendation**: Suggests the most suitable fertilizer based on soil’s current N, P, K levels.

## Project Structure
```
soil-quality-prediction/
├── data/
│   ├── soilpH_rgb1.csv                   # CSV file containing RGB values with pH labels
│   ├── Crop_recommendation_edited.csv   # CSV file containing crop recommendations based on pH
│   └── Fertilizer Prediction.csv        # CSV file containing NPK values of fertilizers
├── images/
│   └── soil-test.webp                   # Example soil image for RGB extraction
├── src/
│   └── soil_quality_prediction.ipynb    #Jupyter Notebook for soil quality prediction
├── README.md                            # Project overview and setup instructions
├── requirements.txt                     # List of dependencies
├── .gitignore                           # Specifies files to ignore in the repo
└── LICENSE                              # License information
```

## Setup Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/moulikaboga/IMAGE-BASED-SOIL-QUALITY-PREDICTION-USING-RGB-ANALYSIS-AND-MACHINE-LEARNING.git
   cd IMAGE-BASED-SOIL-QUALITY-PREDICTION-USING-RGB-ANALYSIS-AND-MACHINE-LEARNING
   ```

2. **Install dependencies**:
   Ensure Python and pip are installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the script**:
   Place your own soil image in the `images/` directory or use the existing `soil-test.webp`. Run the main script:
   ```bash
   python src/soil_quality_prediction.py
   ```

## Usage
The program follows these steps:
1. Loads a soil image, extracts RGB values, and selects a random RGB sample.
2. Trains a Random Forest model on RGB and pH data to predict the soil pH based on RGB input.
3. Retrieves crop recommendations based on the predicted pH value.
4. Suggests the most suitable fertilizer based on the soil’s nutrient needs (N, P, K).

Example output:
```
Predicted pH value (Random Forest): 6.5
At pH 6.5:
Nitrogen (N): 40
Phosphorus (P): 30
Potassium (K): 20
Recommended Crop: Wheat
Recommended Fertilizer: Fertilizer A
```

## Data Sources
- `soilpH_rgb.csv`: Provides RGB values with corresponding pH levels for model training.
- `Crop_recommendation_edited.csv`: Contains crop recommendations for different pH ranges.
- `Fertilizer Prediction.csv`: Lists fertilizers with N, P, K compositions.

## License
This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

---

