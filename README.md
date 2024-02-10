# Suhora Internship Task

## Initial Dataset Exploration and Preprocessing

The first step in the Suhora internship task involved loading the dataset, which consisted of 5604 SAR (Synthetic Aperture Radar) images. These images were annotated with both segmentation and bounding box annotations. The initial exploration and preprocessing of the dataset were performed in the Jupyter Notebook located at [./code/InitialWork.ipynb](./code/InitialWork.ipynb).

## Conversion to YOLO Annotation Format

To prepare the dataset for training with YOLOv8, the MS COCO annotations were converted to the YOLO annotation format. This conversion was carried out using the script available at [./code/COCOtoYOLO.py](./code/COCOtoYOLO.py).

## Dataset Splitting

The dataset was split into three separate folders: train, test, and validation. The train, test, and validation data were located at [./Data/train](./Data/train), [./Data/test](./Data/test), and [./Data/val](./Data/val) respectively. Each of these folders contained two subfolders named `images` and `labels`, where the images were stored in the `images` subfolder and their corresponding annotations were stored in the `labels` subfolder. After the splitting process, there were 3922 images in the train set, 842 images in the test set, and 840 images in the validation set.

## Model Training with YOLOv8

The YOLOv8 model, which is the state-of-the-art model for object detection, was trained on the dataset. The training process was documented in the Jupyter Notebook located at [./Code/Yolov8.ipynb](./Code/Yolov8.ipynb). The model was trained for 100 epochs with a learning rate of 0.01, an image size of 800x800, and early stopping patience set to 10. All the results obtained during the training process were saved at [./runs/detect/train](./runs/detect/train). This directory contains plots, train and validation batch labels, and the trained model weights are saved at [./runs/detect/train/weights](./runs/detect/train/weights).

## Prediction with the Trained Model

Finally, the trained YOLOv8 model was used to make predictions on the entire test dataset. The predictions were saved at [./runs/detect/predict](./runs/detect/predict).

### Sample Predictions
![Prediction 1](./runs/detect/predict/prediction1.jpg)
![Prediction 2](./runs/detect/predict/prediction2.jpg)
![Prediction 3](./runs/detect/predict/prediction3.jpg)
