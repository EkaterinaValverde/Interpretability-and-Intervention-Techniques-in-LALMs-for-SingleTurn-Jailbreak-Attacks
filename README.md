# Interpretability and Intervention in Large Audio-Language Models under Single-Turn Jailbreak Attacks

This repository contains the code and resources developed for the Bachelor's
Thesis on Interpretability and intervention of Large Audio-Language Models
(LALMs) under single-turn audio jailbreak attacks.

The project investigates whether information related to model compliance and
refusal can be identified in internal model representations and whether these
representations can be manipulated through activation steering.

## Overview

The experimental pipeline consists of four main stages:

1. **Dataset construction**
   - Selection and reconstruction of audio jailbreak examples.
   - Generation of a homogeneous audio corpus using text-to-speech.

2. **Activation extraction**
   - Extraction of hidden representations from the audio encoder and
     language-model streams.

3. **Linear probing**
   - Analysis of whether clean/attacked inputs and obey/reject outcomes can
     be linearly recovered from model activations.

4. **Activation steering**
   - Intervention on selected internal representations to investigate their
     effect on model refusal behaviour.

## Models

The experiments were conducted on three open-weight Large Audio-Language Models:

- Voxtral Mini
- Voxtral Small
- Qwen2-Audio

## Dataset

The final dataset contains 200 baseline--attacked pairs, corresponding to
400 audio inputs. It includes three attack strategies: GCG, DNA, and PAIR.

The audio corpus was generated from the corresponding textual records using
a fixed text-to-speech configuration.

## Repository structure

```text
.
├── data/
├── scripts/
├── results/
├── requirements.txt
├── README.md
└── .gitignore
````
The scripts/ directory is organised according to the main stages of the
experimental pipeline: dataset construction, audio generation, activation
extraction, analysis, and activation steering.

## Installation
Clone the repository and install the required dependencies:

```text
git clone YOUR_REPOSITORY_URL
cd YOUR_REPOSITORY_NAME
pip install -r requirements.txt
```

## Usage
The main experimental pipeline consists of:

1. Preparing the dataset
2. Generating the audio files
3. Extracting model activations
4. Training the linear probes
5. Evaluating the probing results
6. Performing activation steering
   
See the corresponding scripts and notebooks for the implementation details.

## Results

The experiments investigate two main questions:
- Can the model distinguish clean and attacked inputs from its internal
representations?
- Can the model's obey/reject behaviour be recovered from its internal
representations?

The repository also contains the code used to perform activation steering and
analyse its effect on refusal behaviour.

## Reproducibility

The experiments use fixed random seeds where applicable. The audio corpus is
generated from the stored textual records using a fixed text-to-speech
configuration.

## Thesis
This repository accompanies the Bachelor's Thesis:
**Interpretability-and-Intervention-Techniques-in-LALMs-for-SingleTurn-Jailbreak-Attacks**
Ekaterina Valverde Bilenko -- Universidad Carlos III de Madrid, 2026 






































