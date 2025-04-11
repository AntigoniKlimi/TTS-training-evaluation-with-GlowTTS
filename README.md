# Glow-TTS Training and Evaluation Project

## Overview

The first part of this project focuses on the training and evaluation of a Glow-TTS model. Glow-TTS is a flow-based text-to-speech model that allows for high-quality and natural speech synthesis. In this project, the model was trained using a subset of the LJSpeech dataset, specifically focusing on speaker002. This repository documents the methodology and steps followed during training, including data preparation, model configuration, and training execution.

## Goal

The primary goal of training the Glow-TTS model is to develop a system capable of generating natural and high-quality synthetic speech from text. By using the LJSpeech dataset and limiting the training to a single speaker, the model aims to achieve speaker-specific fidelity and intelligibility in the synthesized speech.

## Methodology

### Data Source

The dataset used for training is the [LJSpeech dataset]([https://keithito.com/LJ-Speech-Dataset/](https://keithito.com/LJ-Speech-Dataset/)), which consists of approximately 13,100 audio samples along with their corresponding transcriptions. Due to its size and linguistic richness, the LJSpeech dataset is a popular choice for training TTS models.

### Data Preparation

1. **Storage Setup**: Google Drive was configured as a storage backend for managing the training files.
2. **Speaker Selection**: Only samples from `speaker002` were used.
3. **Text Processing**: Each audio file was matched with its corresponding normalized transcript.
4. **Normalization**:
   - Punctuation marks were removed.
   - Numbers were written out in lowercase (e.g., `9` → `nine`).
   - Text was cleaned to improve compatibility with the TTS system.

### Training

The model was trained using the preprocessed data for a 250  epochs, allowing for an initial evaluation of speech quality and intelligibility.

## Evaluation

To evaluate the performance of the trained model, the **Mean Opinion Score (MOS)** was used. This is a subjective metric where listeners rate the quality of synthesized speech on a scale from 1 (bad) to 5 (excellent).  
The results indicated that while the sentences were mostly understandable, the output quality was still limited due to the relatively short training time.

| Evaluation ID | Score | MOS           |
|---------------|-------|----------------|
| Sample 1      | 39/18 | ≈ 2.17         |
| Sample 2      | 36/18 | = 2.00         |
| Sample 3      | 38/18 | ≈ 2.11         |
| Sample 4      | 42/18 | ≈ 2.33         |
| Sample 5      | 35/18 | ≈ 1.94         |

## Conclusions

Training a Glow-TTS model requires careful data preprocessing and appropriate configuration of training parameters. The current results show potential, but the model's performance is still limited due to the small number of training epochs. For significantly improved audio quality, it is recommended to train the model for **500 to 1000 epochs**.

---

## Future Work

- Train for additional epochs to improve speech clarity and naturalness.
- Explore multi-speaker scenarios.
- Integrate voice conversion or speaker adaptation methods.

---

## License

This project is for academic purposes. Please cite the original Glow-TTS and LJSpeech repositories if you use this work in your own research.

Antigoni Klimi

