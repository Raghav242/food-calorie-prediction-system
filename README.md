# Food Calorie Prediction

A Google Colab notebook that identifies food in a photo and retrieves an approximate calorie value. It trains an EfficientNetV2B0 classifier on the 101 categories in the Food-101 dataset, reports the predicted category and confidence, and searches USDA FoodData Central for a matching energy value.

## Run it

1. Open [`calorie-prediction.ipynb`](calorie-prediction.ipynb) in Google Colab and enable a GPU runtime.
2. Run the notebook in order to install dependencies, download Food-101, train and evaluate the model, and save the `.keras` model and class names to Google Drive. Training and downloading can take significant time.
3. For later predictions, mount the same Google Drive and run the notebook's saved-model loading and prediction cells; training is not needed again.
4. Upload a food photo when prompted. The notebook displays the predicted food, confidence, matched USDA food, and energy value. A USDA FoodData Central API key is required for the nutrition lookup.

## Possible applications

The classifier and nutrition lookup could form the starting point for a meal-logging app, a nutrition education tool, or an image-assisted food diary. An application would need a way to confirm the food and enter portion size to estimate calories for an actual serving.

**Limitation:** The image model recognizes a food category; it cannot measure serving size, ingredients, or preparation method. The USDA value is for a matched database record and is not the measured calories in the photo.
