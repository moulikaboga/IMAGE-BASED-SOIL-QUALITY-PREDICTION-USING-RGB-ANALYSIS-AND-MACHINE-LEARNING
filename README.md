# IMAGE-BASED-SOIL-QUALITY-PREDICTION-USING-RGB-ANALYSIS-AND-MACHINE-LEARNING
This project predicts soil pH from RGB values in soil images, offering tailored crop and fertilizer recommendations based on nutrient needs. A Random Forest model estimates pH, which guides crop suitability and suggests fertilizers optimized for nitrogen (N), phosphorus (P), and potassium (K) levels, promoting efficient, data-driven soil management
Soil Quality Prediction and Fertilizer Recommendation System
Project Overview
This project uses machine learning to predict soil quality through pH estimation based on RGB values from soil images. By analyzing these images, we can approximate the pH level and then recommend suitable crops and fertilizers, contributing to optimized soil management and sustainable agricultural practices. The main objectives include:

Extracting RGB values from soil images
Predicting soil pH values based on RGB input using a Random Forest Regressor model
Recommending crops based on the pH level
Suggesting fertilizers based on the soil’s nitrogen (N), phosphorus (P), and potassium (K) requirements
Features
Soil pH Prediction: Predicts the pH of the soil based on RGB values using a trained Random Forest model.
NPK Analysis: Retrieves nitrogen, phosphorus, and potassium levels for different pH levels, helping determine soil nutrient quality.
Fertilizer Recommendation: Suggests the most suitable fertilizer based on soil’s current N, P, K levels.
Project Structure
graphql
Copy code
soil-quality-prediction/
├── data/
│   ├── soilpH_rgb.csv                  # CSV file containing RGB values with pH labels
│   ├── Crop_recommendation_edited.csv   # CSV file containing crop recommendations based on pH
│   └── Fertilizer Prediction.csv        # CSV file containing NPK values of fertilizers
├── images/
│   └── soil-test.webp                   # Example soil image for RGB extraction
├── src/
│   └── soil_quality_prediction.py       # Main script for soil pH prediction and fertilizer recommendation
├── README.md                            # Project overview and setup instructions
├── requirements.txt                     # List of dependencies
├── .gitignore                           # Specifies files to ignore in the repo
└── LICENSE                              # License information
Setup Instructions
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/soil-quality-prediction.git
cd soil-quality-prediction
Install dependencies: Ensure Python and pip are installed, then run:

bash
Copy code
pip install -r requirements.txt
Run the script: Place your own soil image in the images/ directory or use the existing soil-test.webp. Run the main script:

bash
Copy code
python src/soil_quality_prediction.py
Usage
The program follows these steps:

Loads a soil image, extracts RGB values, and selects a random RGB sample.
Trains a Random Forest model on RGB and pH data to predict the soil pH based on RGB input.
Retrieves crop recommendations based on the predicted pH value.
Suggests the most suitable fertilizer based on the soil’s nutrient needs (N, P, K).
Example output:

mathematica
Copy code
Predicted pH value (Random Forest): 6.5
At pH 6.5:
Nitrogen (N): 40
Phosphorus (P): 30
Potassium (K): 20
Recommended Crop: Wheat
Recommended Fertilizer: Fertilizer A
Data Sources
soilpH_rgb.csv: Provides RGB values with corresponding pH levels for model training.
Crop_recommendation_edited.csv: Contains crop recommendations for different pH ranges.
Fertilizer Prediction.csv: Lists fertilizers with N, P, K compositions.
License
This project is licensed under the Apache License 2.0 - see the LICENSE file for details.
