# Semi-Supervised Classification of Diabetic Foot Ulcers

This repository contains the code developed for my MSc Data Science
dissertation investigating pseudo-labelling for the classification of
infection and ischaemia in diabetic foot ulcer images using the
DFUC2021 dataset.

## Project Overview

The project investigates whether unlabelled DFUC2021 images can improve
four-class classification performance through semi-supervised
pseudo-labelling.

The four classes are:

- None
- Infection
- Ischaemia
- Both infection and ischaemia

An ImageNet-pretrained EfficientNet-B3 was used as the supervised
baseline and teacher model. The experiments investigated:

- Global pseudo-label confidence thresholds
- Class-specific pseudo-label selection
- Minority-class data augmentation
- Minority-class augmentation combined with pseudo-labelled data
- Minority-class augmentation without pseudo-labelled data

## Dataset

The experiments use the DFUC2021 dataset.

The dataset is not included in this repository and must be obtained
separately from the official DFU Challenge source.

## Main Results

The supervised EfficientNet-B3 baseline achieved a test macro F1-score
of 0.5448.

The highest test macro F1-score of 0.5507 was obtained by combining
pseudo-labels retained at a confidence threshold of 0.97 with targeted
minority-class augmentation.

## Repository Contents

The notebooks contain the implementation of the supervised baseline,
pseudo-label generation and threshold selection, class-specific
pseudo-label experiments, and minority-class augmentation experiments.

## Requirements

The project was implemented in Python using libraries including:

- PyTorch
- torchvision
- pandas
- NumPy
- scikit-learn
- torchmetrics
- Matplotlib
- Pillow
- tqdm
