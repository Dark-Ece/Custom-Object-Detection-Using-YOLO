# Retail Product Detection Using YOLO

## Project Overview

This project implements a custom object detection model using the YOLO (You Only Look Once) framework to detect and classify retail products in images.

The model was trained on a custom-labeled dataset containing four product categories:

* Coffee
* Nivea
* Noodles
* Perfume

The project demonstrates the complete computer vision workflow, including dataset annotation, training, evaluation, and deployment of a custom YOLO model.

---

## Features

* Multi-class product detection
* Real-time object detection
* Custom dataset training
* Bounding box visualization
* High-accuracy product recognition
* Easy deployment for image inference

---

## Dataset Classes

The model is trained to detect the following classes:

| Class ID | Product |
| -------- | ------- |
| 0        | Coffee  |
| 1        | Nivea   |
| 2        | Noodles |
| 3        | Perfume |

---

## Tools & Technologies Used

### Development Environment

* Google Colab

### Programming Language

* Python

### Deep Learning Framework

* Ultralytics YOLO

### Annotation Tool

* Label Studio

### Libraries

* PyTorch
* OpenCV
* NumPy
* Pandas
* Matplotlib

### Version Control

* Git
* GitHub

---

## Dataset Annotation

Images were manually annotated using Label Studio and exported in YOLO format for training.

Dataset Structure:

dataset/

├── train/

│ ├── images/

│ └── labels/

├── valid/

│ ├── images/

│ └── labels/

└── data.yaml

---

## Model Training

The model was trained using the Ultralytics YOLO framework on Google Colab.

### Training Configuration

* Framework: YOLO
* Training Platform: Google Colab
* Annotation Tool: Label Studio
* Epochs: 60

---

## Performance Metrics

### Best Validation Results

| Metric    | Value  |
| --------- | ------ |
| Precision | 98.08% |
| Recall    | 97.50% |
| mAP@50    | 99.50% |
| mAP@50-95 | 64.96% |

### Final Training Loss

| Loss Type           | Value |
| ------------------- | ----- |
| Box Loss            | 0.629 |
| Classification Loss | 0.382 |
| DFL Loss            | 0.949 |

---

## Project Structure

project/

├── README.md

├── requirements.txt

├── best.pt

├── train.ipynb

├── results/

│ ├── results.png

│ ├── confusion_matrix.png

│ ├── PR_curve.png

│ └── F1_curve.png

└── sample_images/

---

## Running Inference

```python
from ultralytics import YOLO

model = YOLO("best.pt")

results = model("image.jpg", save=True)
```

---

## Applications

* Smart Retail Systems
* Inventory Monitoring
* Automated Shelf Analysis
* Product Recognition
* Retail Analytics
* Computer Vision Research

---

## Future Improvements

* Increase dataset size
* Add more product categories
* Real-time video detection
* Edge AI deployment
* Mobile application integration

---

## Author

Sahil Thakur

B.Tech Electronics & Communication Engineering (ECE)

Jawaharlal Nehru Government Engineering College (JNGEC)

---

## License

This project is intended for educational and research purposes.
