# Chest X-ray Classifier · Lab 15

Download the [Android Studio project](steeven_eugenio_lab15.zip), unzip it, and open the extracted project folder in Android Studio.

**Steeven Eugenio · Yachay Tech**

An educational Android app that runs a CNN exported to TensorFlow Lite and classifies four bundled pediatric chest radiographs as Normal or Pneumonia. It uses the same model and PNG files as the accompanying notebook.

## Run

1. Open this directory in Android Studio and sync Gradle. Use JDK 17 or later and install Android SDK 35.
2. Start an Android Virtual Device (API 23 or later) or connect a device.
3. Run `app` and select **Case 1** through **Case 4**. The output is the predicted dataset label and its model score.

## Model and inputs

`app/src/main/assets` contains the model and four 28 × 28 grayscale PNGs. The app converts each pixel to float32 and divides it by 255. Output indices 0 and 1 map to Normal and Pneumonia, respectively. `results.json` records the notebook's official test accuracy, confusion matrix and case predictions.

Run the accompanying `steeven_eugenio_lab15.ipynb` in Google Colab to retrain on PneumoniaMNIST and recreate the assets in `lab15_artifacts/`. To use a newly trained model, copy the new `.tflite` and the four matching PNGs into the Android assets directory and rebuild.

Data: [PneumoniaMNIST, MedMNIST v2](https://medmnist.com/) · [Zenodo](https://doi.org/10.5281/zenodo.10519652) · CC BY 4.0.
