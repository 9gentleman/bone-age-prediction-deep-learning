# Bone Age Prediction from Wrist X-Ray Images Using Deep Learning

This project focuses on estimating pediatric bone age from wrist X-ray images using deep learning models. It includes medical image preprocessing, regression-based prediction, model comparison, and a multi-input deep learning architecture.

The main objective is to predict bone age in months from pediatric wrist radiographs and compare the performance of different deep learning architectures.

## Project Overview

Bone age assessment is commonly used in clinical practice to evaluate skeletal development, growth disorders, hormonal conditions, and developmental abnormalities.

Traditional methods such as Greulich-Pyle and Tanner-Whitehouse require expert interpretation and may be time-consuming. In this project, deep learning models are used to automate bone age prediction from wrist X-ray images.

The project also investigates whether adding gender information improves prediction performance.

## Dataset

The project uses the RSNA Pediatric Bone Age Dataset.

The dataset contains pediatric wrist X-ray images, bone age labels in months, and gender information.

The dataset is not included in this repository due to file size and external dataset access requirements.

## Project Files

* `notebooks/bone_age_test.ipynb`
  Notebook for model training, testing, and comparison of CNN and transfer learning models.

* `notebooks/bone_age_multiinput.ipynb`
  Notebook for the multi-input DeepCNN model using both wrist X-ray images and gender information.

* `report/bone-age-prediction-deep-learning-report.pdf`
  Full project report.

* `outputs/figures/`
  Contains generated visual outputs such as model comparison charts, prediction plots, data distribution graphs, and confusion matrix figures.

* `outputs/reports/`
  Contains exported result tables, benchmark reports, and evaluation outputs.

* `outputs/models/`
  Contains trained model outputs if file sizes are suitable for GitHub. Large trained model files may be excluded.

## Methods

The project includes the following steps:

* Data loading and validation
* Wrist X-ray image preprocessing
* Image resizing and normalization
* Train / validation / test split
* CNN-based regression modeling
* Transfer learning model comparison
* Multi-input model development using image and gender data
* Model evaluation with regression metrics
* Age group classification and confusion matrix analysis
* Output generation for figures, reports, and model results

## Models Compared

The following models were evaluated:

* SimpleCNN
* DeepCNN
* MobileNetV2
* EfficientNetB0
* DenseNet121
* DeepCNN Multi-Input

## Results

The best performance was achieved by the DeepCNN Multi-Input model, which uses both X-ray images and gender information.

| Model               |          MAE |         RMSE |     R² |
| ------------------- | -----------: | -----------: | -----: |
| DeepCNN             | 17.61 months | 23.67 months | 0.6721 |
| DeepCNN Multi-Input | 15.35 months | 21.79 months | 0.7221 |

Adding gender information improved the model performance and reduced the MAE from 17.61 months to 15.35 months.

## Technologies Used

* Python
* TensorFlow
* Keras
* Pandas
* NumPy
* Matplotlib
* Seaborn
* scikit-learn
* Jupyter Notebook

## Repository Structure

```text
bone-age-prediction-deep-learning/
│
├── README.md
│
├── notebooks/
│   ├── bone_age_test.ipynb
│   └── bone_age_multiinput.ipynb
│
├── report/
│   └── bone-age-prediction-deep-learning-report.pdf
│
└── outputs/
    ├── figures/
    ├── reports/
    └── models/
```

## Notes

The dataset is not included in this repository because of its large size.

Large trained model files may also be excluded due to GitHub file size limitations.

The project report and notebooks explain the experimental process, model architectures, evaluation metrics, and results.
