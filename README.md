# Brand-Detection-Model

Real-Time Brand Detection Using YOLOv8 and OCR

Overview

This project implements a real-time brand detection system using YOLOv8 for object detection and OCR for extracting product details like MRP and expiry date. The system detects and counts products from five different brands in a live video feed, with tracking capabilities and automatic data extraction upon receiving a stop signal.

Dataset Collection & Preprocessing

## Dataset Details:

344 images captured from local supermarkets.

Brands annotated in YOLOv8 format.

Preprocessing Steps:

Auto-orientation of pixel data (with EXIF-orientation stripping).

Resized to 640x640 (stretch method).

## Data Augmentation:

Each source image was transformed into 3 augmented versions using:

Random 90-degree rotations: None, clockwise, counter-clockwise, upside-down (equal probability).

Random rotation between -15° and +15°.

Random brightness adjustment between -10% and +10%.

Bounding Box Transformations:

Random shear between -5° to +5° horizontally and -5° to +5° vertically.

Salt and pepper noise applied to 0.85% of pixels.

## Model Training & Integration

Trained YOLOv8 model on the processed dataset.

Optimized model weights for deployment.

Integrated the trained model into a web application for live brand detection.

## Features

✅ Live webcam-based brand detection  
✅ Efficient object tracking using Norfair  
✅ OCR-based extraction of MRP & expiry date  
✅ Optimized for real-time performance  

## How It Works

The model runs on a live video feed and detects branded products.

When the stop signal is received, it displays a table of detected brands and counts.

The camera is reactivated to extract label details (MRP & expiry date) for a representative product of each brand.

The details are processed and displayed before moving to the next brand.

Installation & Setup

# Clone the repository
git clone https://github.com/yourusername/your-repo.git
cd your-repo

# Install dependencies
pip install -r requirements.txt

# Run the detection script
python detect.py

## Technologies Used

YOLOv8 for object detection

Norfair for object tracking

Tesseract OCR for text extraction

OpenCV for image processing

Flask (or Streamlit) for the web interface

Future Improvements

Improving OCR accuracy with fine-tuned text recognition models.

Extending to more brands and different product categories.

Deploying as a cloud-based API for wider accessibility.

-Kaggle Notebook: https://www.kaggle.com/code/ajeffreyrufus/brand-detection-model  
-Kaggle dataset: https://www.kaggle.com/datasets/ajeffreyrufus/brand-detection-dataset-unique-id-2024-11-03
