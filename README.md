# Project: Food Packaging Image Analysis

This project aims to analyze images of food packaging (e.g., snack bags, breakfast items, spaghetti boxes, salad bags, canned goods) and identify the following elements on these packages:

- Text areas (e.g., ingredient lists)
- Specific marking areas (barcodes, QR codes)
- Graphic elements areas (Logos, characters, etc.)

The project uses a combination of image processing and machine learning techniques to achieve this.

## Code Overview

The code is written in Python and uses several libraries including `cv2`, `matplotlib`, `pytesseract`, `pandas`, `numpy`, `PIL`, and `ultralytics`.

The main components of the code are:

- **Import of required libraries**: The necessary Python libraries are imported. Some libraries are installed using pip and apt-get.

- **Library**: Two classes `TextDetector` and `YoloDetector` are defined. `TextDetector` is used to extract and highlight text from images. `YoloDetector` is used to train a YOLO model and make predictions.

- **Intersection over Union (IoU)**: A function `bb_intersection_over_union` is defined to calculate the IoU of two boxes. Another function `eliminate_overlapping_boxes` is used to eliminate boxes that overlap with boxes in another array.

- **Plotting**: Functions `plot_boxes` and `plot_img` are defined to plot bounding boxes on images and display images.

- **Inference**: A function `inference` is defined to perform inference on a list of images.

- **Training**: A SAM model is loaded and a YOLO model is trained.

- **Performances on fine-tuning**: The performance of the model is evaluated.

- **Prediction**: Predictions are made using the trained YOLO and SAM models.

## Current State

The Yolo model achieves a mean average precision (mAP) of 0.6485 on the test set. 

## Usage

To use this project, you need to have the necessary Python libraries installed. You can then run the code in the `vn.ipynb` notebook. The notebook includes sections for training the model and making predictions.

## Note

This project is a work in progress. Future updates may include improvements to the model and additional features.

The dataset used for training the model is not included in this repository. You can use have a look at the dataset [here](https://drive.google.com/drive/folders/15xmW4FKnEUTmYFol3AWG3PcIwBnWyNcV?usp=sharing). 

Big thanks to *LEMELIN William* for providing the dataset.