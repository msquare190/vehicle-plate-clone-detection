Vehicle Plate Clone Detection – MSc Dissertation Project

This repository contains the code for my MSc Data Science dissertation:

> Enhancing Vehicle Identification Systems: A Deep Learning Approach to Detecting Cloned and Anomalous License Plates in the UK

The project focuses on detecting cloned vehicle number plates using a combination of:

- Licence plate detection (YOLOv8)
- Optical Character Recognition (OCR) for reading registration numbers (EasyOCR)
- Vehicle Re-Identification (ReID) using deep CNN embeddings (ResNet50)
- A simple temporal–spatial anomaly module to approximate impossible plate movements
- A web-based Streamlit demo for interactive exploration



 Overview

In many real-world scenarios, criminals reuse (“clone”) a legitimate vehicle registration number on a different vehicle to evade detection. Traditional ANPR systems mainly focus on detection and OCR accuracy, not on behavioural anomalies.

This project simulates and analyses cloned-plate scenarios by:

1. Generating a synthetic clone dataset by overlaying UK-style plates onto multiple vehicles.
2. Extracting:
   - Plate text + OCR confidence  
   - Vehicle appearance embeddings  
   - Synthetic time and location metadata  
3. Computing a clone suspicion score that fuses:
   - Visual difference between vehicles  
   - OCR uncertainty  
   - Temporal anomaly (speed implied between sightings)  
4. Evaluating performance and performing ablation studies.
5. Providing a Streamlit app for visual, interactive demos.


Dataset Access

This project uses two publicly available datasets:

- Kaggle UK Synthetic Licence Plate Dataset  
  https://www.kaggle.com/datasets/saadbinmunir/uk-licence-plate-synthetic-images

- Roboflow License Z4TOU Vehicle & Plate Dataset  
  https://universe.roboflow.com/license-rl231/license-z4tou


