# DanceGPT2

Welcome to DanceGPT2.

This repository contains code for training a GPT-2 model to unconditionally generate dance music. By leveraging the high fidelity neural audio compression codec, EnCodec, audio is converted into a set of codes which are then fed to the GPT-2 Decoder-only Transformer. After training, the model can create new dance music tracks.

`training.ipynb` has additional routines capable of generating longer examples as well as continuing existing music.

## Overview

The project focuses on generating dance music using the following workflow:
1. **Audio Compression**: Using the EnCodec codec to convert audio segments into a sequence of tokens or "codes".
2. **Training GPT-2**: Training the GPT-2 model on the tokenized audio data.
3. **Music Generation (Inference)**: Prompting the trained GPT-2 model to generate the aforementioned "codes", then decoding via EnCodec to create new dance music tracks.

## Repository Contents

- `training.ipynb`: A Jupyter notebook containing the full training pipeline for the GPT-2 model.
- `longer_audio_samples/`: A folder with long audio samples generated by the model.

## Trained Model Weights

To load the model weights from a checkpoint, please find the `model.safetensors` file in [this](https://huggingface.co/JulianS/DanceGPT2/tree/main) HuggingFace repository and use the location of the file as the `checkpoint_dir` in the `training.ipynb` codebook. 
