# NYC Airbnb ML Pipeline - Project Submission

## Student Information
- Name: [Your Name]
- Project: Build an ML Pipeline for Short-Term Rental Prices

## Project Links
- **W&B Project**: https://wandb.ai/bpolich-western-governors-university/nyc_airbnb
- **GitHub Repository**: https://github.com/bpolich-code/Project-Build-an-ML-Pipeline-Starter
- **Release v1.0.0**: https://github.com/bpolich-code/Project-Build-an-ML-Pipeline-Starter/releases/tag/1.0.0

## Project Results

### Model Performance
- **Model**: Random Forest Regressor
- **Test Set R² Score**: 0.564
- **Test Set MAE**: $33.85
- **Sample2 R² Score**: 0.580
- **Sample2 MAE**: $32.42

### Hyperparameter Optimization
Trained 5 models with different hyperparameters:
- max_depth: 10, 15, 50
- n_estimators: 100, 200

All models achieved similar performance (MAE ~$34), selected model with max_depth=10, n_estimators=100 as production model.

### Pipeline Steps Completed
1. ✅ Data Download
2. ✅ Exploratory Data Analysis
3. ✅ Data Cleaning
4. ✅ Data Testing
5. ✅ Train/Test Split
6. ✅ Train Random Forest (with hyperparameter optimization)
7. ✅ Model Testing
8. ✅ Pipeline Release (v1.0.0)
9. ✅ Testing on New Data (sample2.csv)

## Running the Pipeline

To run the complete pipeline:
```bash
mlflow run https://github.com/bpolich-code/Project-Build-an-ML-Pipeline-Starter.git -v 1.0.0
```

To run on new data:
```bash
mlflow run https://github.com/bpolich-code/Project-Build-an-ML-Pipeline-Starter.git \
  -v 1.0.0 \
  -P hydra_options="etl.sample='sample2.csv'"
```
