# AAI-590: Capstone Project - Deepfake Detection with Convolutional Models and Vision Transformers

This project is part of the AAI-590 course in the Applied Artificial Intelligence Program at the University of San Diego (USD)

**- Project Status: Completed**

## Installation

The included Jupyter Notebooks are intended to be run in the Google Colab environment. If running locally, the following dependencies are required:
```
torch
pyiqa
```

## Project Objective

The goal of this project was to evaluate two different neural model architectures, CNN and ViT, on the task of Deepfake detection and compare them. Also, the effects of different kinds of image distortion and artifacts on these models accuracies was studied. Then, the results of this analysis can be used for the development of deep fake detection applications. This project focuses on images featuring people faces.

## Contributor

Priscilla Marquez

## Methods Used

* Computer Vision
* Deep Learning
* IQA
* Data Visualization

## Technologies

* Python
* PyTorch

## Project Description

This project showcases the model selection, training and evaluation process of a CNN and ViT on the task of Deepfake recognition applied to face images. The dataset used was [Deepfake and Real images](https://www.kaggle.com/datasets/manjilkarki/deepfake-and-real-images). This dataset contains a large selection of face images, both real and artificially generated, cleanly labeled, preprocessed and divided into Training, Test and Evaluation splits. The models themselves were built and trained with PyTorch. Then, during the evaluation process, the effects of distorting correctly classified images with Gaussian noise, blur and JPEG compression were tested to discover the strengths and weaknesses of each architecture when applied to this task.

The most important files in the repository are the three `.ipynb` Notebook files. These will work better if they are run through Google Colab. The following subsections describe the content of each individual notebook.

### Capstone Dataset Cleanup

This notebook includes the initial dataset exploration code. It helps visualize the contents of the dataset and also performs EDA through three different approaches:

* Basic pixel statistics: histograms of the distribution of the pixel values through the different dataset splits
* Image Quality Assesment (IQA): analysis of the images through IQA algorithms to try and find biases in the image quality
* Facial Attribute Recognition: use of neural models to generate statistics about the faces in the dataset (age, gender, emotion...), although this step was not featured in the final report.

### Capstone Training

Main notebook, it is divided into four main sections:

* **Dataset**: contains the code required to load the dataset and preprocess it for PyTorch model consumption
* **Training**: contains the common training loop code used through the remainder of the project
* **CNN**: contains the training and testing process for the CNN model
* **ViT**: contains the training and testing proceess for the ViT model

Both the **CNN** and **ViT** sections contain the following subsections:

* **Ablation testing**: search through possible model parameters to find the best configuration
* **Best model training**: final training of the model through all the Training split
* **Model testing**: evaluation of the resulting model

### Capstone Demo

This notebook contains the proof of concept demonstrated in the presentation video.

## License

Apache-2.0
