# End-to-End-Multilingual-Speech-Recognition-Training-Pipeline

## Overview

This repository presents an end-to-end Automatic Speech Recognition (ASR) training pipeline developed for multilingual speech recognition. It demonstrates the complete machine learning workflow, beginning with raw audio preprocessing and dataset preparation, followed by model fine-tuning, evaluation, and inference.

The primary objective of this project is to build a scalable and reproducible training pipeline capable of handling multilingual speech data while maintaining high data quality and efficient model training practices.

> **Note:** The original dataset used in this project is proprietary and cannot be publicly shared due to confidentiality agreements. This repository has been prepared as a portfolio version to demonstrate the complete engineering and research workflow without exposing sensitive data.

---

# Features

- End-to-end speech recognition pipeline
- Automated audio preprocessing
- Metadata generation
- Dataset validation
- Training and validation dataset preparation
- Transformer-based model fine-tuning
- Model evaluation
- Inference pipeline
- Modular project structure
- Configuration-driven workflow

---

# Workflow

```text
                    Raw Audio Dataset
                           │
                           ▼
                  Dataset Validation
                           │
                           ▼
                 Audio Preprocessing
                 • Resampling (16 kHz)
                 • Mono Conversion
                 • Audio Normalization
                 • File Validation
                           │
                           ▼
                Metadata Generation
                           │
                           ▼
             Train / Validation Split
                           │
                           ▼
                 Feature Extraction
                           │
                           ▼
                Model Fine-Tuning
                           │
                           ▼
                 Model Evaluation
                           │
                           ▼
                    Model Inference
```

---

# Project Structure

```text
.
├── configs/
│   └── config.yaml
│
├── preprocessing/
│   ├── preprocess.py
│   ├── validation.py
│   ├── metadata.py
│   └── utils.py
│
├── training/
│   ├── train.py
│   ├── dataset.py
│   ├── trainer.py
│   └── model.py
│
├── evaluation/
│   ├── evaluate.py
│   └── metrics.py
│
├── inference/
│   └── inference.py
│
├── data/
│   └── sample_audio/
│
├── requirements.txt
│
└── README.md
```

---

# Preprocessing Pipeline

The preprocessing stage prepares raw audio for model training through several quality assurance and normalization steps.

The pipeline includes:

- Audio file validation
- Corrupted file detection
- Audio resampling to 16 kHz
- Mono channel conversion
- Audio normalization
- Transcript validation
- Metadata generation
- Dataset preparation
- Train/Validation split creation

These steps ensure consistency across the dataset and improve the quality of the training data.

---

# Model Training

The training pipeline consists of:

- Dataset loading
- Feature extraction
- Data collation
- Model fine-tuning
- Periodic validation
- Checkpoint saving
- Performance logging

The training workflow has been designed to be modular, making it straightforward to adapt the pipeline to different datasets and transformer-based speech recognition models.

---

# Evaluation

Model performance is evaluated using standard Automatic Speech Recognition metrics.

| Metric | Score |
|---------|-------|
| Word Error Rate (WER) | 27.9517% |
| BLEU Score | 43.882593% |

The evaluation pipeline can easily be extended to include additional metrics such as Character Error Rate (CER) or language-specific evaluations.

---

# Inference

The inference pipeline performs the following steps:

1. Load input audio
2. Apply preprocessing
3. Extract model features
4. Generate transcription
5. Return predicted text

The inference module can be integrated into downstream applications or deployed as a standalone service.

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Whisper
- NumPy
- Pandas
- Librosa
- FFmpeg
- Docker

---

# Repository Goals

This repository demonstrates the implementation of:

- End-to-end machine learning pipelines
- Speech data preprocessing
- Transformer model fine-tuning
- Experiment organization
- Modular software design
- Reproducible research workflows
- Machine learning engineering best practices

---

# Dataset

The dataset used in the original project is **not included** in this repository.

The project was developed using a confidential multilingual speech dataset containing annotated speech recordings. Due to confidentiality and data privacy agreements, the dataset cannot be released publicly.

To reproduce the pipeline, users may substitute any publicly available speech dataset such as:

- Mozilla Common Voice
- LibriSpeech
- FLEURS
- VoxPopuli

or their own speech recordings.

---

# Reproducibility

The repository has been organized to encourage reproducible experimentation through:

- Modular codebase
- Configuration-driven training
- Independent preprocessing and training modules
- Clearly separated evaluation pipeline
- Consistent project structure

---

# Disclaimer

This repository is a portfolio version of an industrial research project.

Certain implementation details, proprietary resources, trained weights, and the original dataset have been intentionally omitted to comply with confidentiality and non-disclosure obligations.

The repository preserves the complete methodology, engineering practices, and overall machine learning workflow while protecting sensitive information.

---

## Author

**Samina**

Machine Learning Engineer

This repository has been developed as part of ongoing research and engineering work in multilingual speech recognition and machine learning systems.

