
# Comparative Analysis of Autoencoders with Different Bottleneck Dimensions

## Project Overview
This project compares two autoencoders with different bottleneck dimensions to study the trade-off between image compression and reconstruction quality.

## Objectives
- Build two autoencoders with different bottleneck dimensions.
- Compare original images with reconstructed images.
- Evaluate reconstruction quality using Mean Squared Error (MSE) and Mean Absolute Error (MAE).
- Analyze compression versus information preservation.

## Dataset
**Fashion-MNIST** is a dataset of grayscale clothing images.

- Training images: 60,000
- Testing images: 10,000
- Image size: 28 × 28 pixels
- Flattened input size: 784 values per image
- Pixel values are normalized to the range 0–1.

## Model Architecture

| Model | Bottleneck dimension | Dimensional compression ratio |
|---|---:|---:|
| Model A | 16 | 49:1 |
| Model B | 64 | 12.25:1 |

The encoder compresses an image into a smaller representation. The decoder reconstructs the image from that representation.

## Methodology
1. Load and normalize the Fashion-MNIST dataset.
2. Build two autoencoder models.
3. Train each model for 10 epochs using the Adam optimizer and binary cross-entropy loss.
4. Compare reconstructed images with original images.
5. Calculate test MSE and MAE.
6. Plot training and validation loss and compare the results.

## Evaluation Metrics
- **MSE:** Mean Squared Error between original and reconstructed pixels.
- **MAE:** Mean Absolute Error between original and reconstructed pixels.

Lower error values indicate better reconstruction under these metrics.

## Results
The experiment generates a comparison table, reconstruction images, and training-loss graphs. Actual metric values should be taken from the experiment's saved results.

## Tools and Technologies
- Python
- Google Colab
- TensorFlow and Keras
- NumPy
- Matplotlib
- Pandas

## How to Run
1. Open the `.ipynb` notebook in Google Colab.
2. Run the cells from top to bottom.
3. Allow the dataset to download.
4. Train both models and inspect the comparison graphs and metrics.

## Conclusion
The experiment investigates how bottleneck size affects reconstruction quality. A smaller bottleneck provides greater dimensional compression, while a larger bottleneck provides more dimensions for representing image information. The measured errors and reconstructed images help evaluate this trade-off.

## References
- Fashion-MNIST: https://github.com/zalandoresearch/fashion-mnist
- TensorFlow: https://www.tensorflow.org/
- Keras: https://keras.io/
