# Bone Age Prediction from Wrist X-Ray Images Using Deep Learning

This project focuses on estimating pediatric bone age from wrist X-ray images using deep learning models. The study was developed as a Software Engineering graduate term project and includes model comparison, medical image preprocessing, regression-based prediction, and a multi-input deep learning architecture.

The main objective of the project is to predict bone age in months from pediatric wrist radiographs and compare the performance of different deep learning architectures.

## Project Overview

Bone age assessment is commonly used in clinical practice to evaluate skeletal development, growth disorders, hormonal conditions, and developmental abnormalities. Traditional methods such as Greulich-Pyle and Tanner-Whitehouse require expert interpretation and may be time-consuming.

In this project, deep learning models were trained and evaluated to automate bone age prediction from wrist X-ray images. The project also investigates whether adding gender information improves model performance.

## Dataset

The project uses the RSNA Pediatric Bone Age Dataset.

The dataset includes pediatric wrist X-ray images and corresponding bone age labels in months. Gender information is also used in the multi-input model.

The dataset itself is not included in this repository due to file size and external dataset access requirements.

## Project Files

* `notebooks/bone_age_test.ipynb`
  Contains model training, testing, and comparison steps for CNN and transfer learning models.

* `notebooks/bone_age_multiinput.ipynb`
  Contains the multi-input DeepCNN model that uses both wrist X-ray images and gender information.

* `report/Can Kutlay - Dönem Projesi.pdf`
  Full academic project report.

* `outputs/figures/`
  Contains generated visual outputs such as model comparison charts, prediction plots, data distribution graphs, and confusion matrix figures.

* `outputs/reports/`
  Contains exported result tables, benchmark reports, and evaluation outputs.

* `outputs/models/`
  Contains trained model outputs if file sizes are suitable for GitHub. Large trained model files may be excluded from the repository.

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

Adding gender information improved model performance and reduced the MAE from 17.61 months to 15.35 months.

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
│   └── Can Kutlay - Dönem Projesi.pdf
│
└── outputs/
    ├── figures/
    ├── reports/
    └── models/
```

## Notes

The dataset is not included in this repository because of its large size. The project report and notebooks explain the experimental process, model architecture, evaluation metrics, and results.

Large trained model files may also be excluded from the repository due to GitHub file size limitations.

## Author

Can Kutlay
