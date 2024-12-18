# Pneumonia Detection Using GAN

This repository contains a Generative Adversarial Network (GAN) model designed to generate realistic images and classify them as either "Pneumonia" or "Normal" based on a dataset of chest X-ray images. The project uses DCGAN and ACGAN architectures to generate synthetic data for training a classifier that can distinguish between pneumonia and normal X-rays. The model leverages the power of deep learning to improve medical diagnostics and enhance AI-based systems.

## Project Overview

<img src="./assets/Architectures-Combined.drawio.png" alt="Architecture"></img>

The main goal of this project is to generate synthetic chest X-ray images and use them to train a binary classifier to predict pneumonia detection. The solution involves the following components:

1. **GAN Architectures**: DCGAN (Deep Convolutional GAN) and ACGAN (Auxiliary Classifier GAN) are used to generate images and extract features.
2. **Feature Extraction**: The last three layers of the GAN discriminator are used to extract features for classification.
3. **Classification**: A binary classifier (XGBoost and LightGBM) is trained using the extracted features to predict the class of new images: pneumonia or normal.
4. **Image Preprocessing**: Images are resized to 256x256 pixels before being fed into the GAN.
5. **Optimization**: Various optimizers, including Adam and RMSprop, and activation functions like ReLU, LeakyReLU, GELU, and ELU are experimented with to improve model performance.

## Requirements

- Python 3.x
- PyTorch 
- Scikit-learn
- XGBoost
- LightGBM
- Matplotlib (for visualizations)
- Seaborn (for visualizations)

## Dataset

The project uses a dataset of chest X-ray images, where each image is labeled as either "Pneumonia" or "Normal." These images are resized to 256x256 pixels to ensure uniformity across the dataset.

## Experiments

- [DCGAN](https://www.kaggle.com/code/sahilsasane/dcgan-analysis)
- [WGAN GP](https://www.kaggle.com/code/sahilsasane/wgan-gp-analysis)
- [ACGAN](https://www.kaggle.com/code/sahilsasane/acgan-analysis)


## Results

This project produces synthetic chest X-ray images that mimic real-world data and helps train a classifier capable of distinguishing between pneumonia and normal X-rays. The experiments with DCGAN and ACGAN show how different GAN architectures can affect the quality of the generated data and the performance of the classifier.

## Future Work

- Experiment with semi-supervised GANs to improve the classifier’s generalization capabilities.
- Introduce data augmentation to enhance the robustness of the model.
- Incorporate transfer learning to leverage pre-trained models for better feature extraction.

## Acknowledgments

- [Kaggle Chest X-ray Pneumonia Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- [PyTorch](https://pytorch.org/)
- [XGBoost](https://xgboost.readthedocs.io/)
- [LightGBM](https://lightgbm.readthedocs.io/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
