# Siamese-U-Net-for-Change-Detection-on-Satellite-Images
This repository contains the implementation of a Siamese U-Net model for detecting changes in satellite images. The model has been trained on the WHU RS Change Detection Dataset and produces a binary change map highlighting regions of significant differences between pre-change and post-change images.
Features
Model Architecture: The Siamese U-Net model leverages two U-Net branches to process pre-change and post-change images independently, followed by a fusion mechanism for change detection.
Dataset: Trained on the WHU RS Change Detection Dataset, which contains annotated high-resolution remote sensing images.
Output: Generates binary images marking regions of change between the input image pairs.
Application: Useful for urban planning, environmental monitoring, disaster assessment, and more.
Model Overview
Siamese U-Net Architecture
The model architecture consists of:

Two identical U-Net branches for feature extraction from pre-change and post-change images.
Shared weights across the branches to ensure the same feature extraction process for both inputs.
Feature fusion layer to combine the outputs of the two U-Net branches.
Binary segmentation output for highlighting regions of change.
Dataset
WHU RS Change Detection Dataset
The dataset comprises:

Pairs of pre-change and post-change satellite images.
Pixel-level binary labels representing areas of change.
Dataset details:

Image resolution: High-resolution remote sensing imagery.
Applications: Urban expansion detection, environmental changes, disaster damage assessment, etc.
For more information on the dataset, visit the WHU RS Dataset Page.

Results
Evaluation Metrics: The model is evaluated using metrics such as Intersection over Union (IoU), Precision, Recall, and F1-Score.

Installation
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/siamese-unet-change-detection.git
cd siamese-unet-change-detection
Install dependencies:
bash
Copy code
pip install -r requirements.txt
Usage
Training the Model
Prepare the dataset:
Download the WHU RS Change Detection Dataset.
Place the dataset in the data/ directory.
Train the model:
bash
Copy code
python train.py --config config.yaml
Testing the Model
To test the model on new satellite image pairs:

bash
Copy code
python test.py --pre_image path/to/pre_image.png --post_image path/to/post_image.png --output path/to/output.png
Requirements
Python 3.8+
TensorFlow/PyTorch (Specify the framework used)
Other dependencies (see requirements.txt)
Acknowledgments
WHU RS Change Detection Dataset creators for providing an excellent dataset for change detection research.
The Siamese U-Net paper and the research community for inspiring this project.
