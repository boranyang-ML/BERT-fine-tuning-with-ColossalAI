# BERT Fine-tuning with ColossalAI

## Overview
This repository contains code for fine-tuning a pre-trained language model "Bidirectional Encoder Representations from Transformers" (BERT) using [ColossalAI](https://github.com/hpcaitech/ColossalAI).

## Model
Model: Bidirectional Encoder Representations from Transformers (BERT: `bert-base-uncased`)

## Dataset
Dataset: GLUE (General Language Understanding Evaluation)

## File Structure
```
  ├── bert.ipynb: the main file for fine-tuning BERT (on Colab), it also contains experiments logs
  ├── requirements.txt: lists all the dependencies needed to run code in this repository
  └── README.md: all the instructions and relative information go here
```

## Parallel Settings
Parallel mode: torch_ddp (PyTorch Distributed Data Parallel)

## Configuration
* The hyperparameter configuration (e.g. `NUM_EPOCHS`, `BATCH_SIZE`, `LEARNING_RATE`, etc.) can be found under the Hyperparameters block in `bert.ipynb`.
* The argument configuration (e.g. `plugin`, `model_type`, etc.) can be found under the Arguments block in the `main()` function in `bert.ipynb`.

## How to run
* Make sure you install the dependencies listed in `requirements.txt` via `pip install -r requirements.txt`
* Alternatively, you can simply follow the `bert.ipynb` notebook to run the code. It also contains the commands for installing all the necessary dependencies.
* You can start running the code by following the `bert.ipynb` notebook on Google Colab.

## Experiment Results

| Plugin         | Accuracy | F1-score | GPU number |
| -------------- | -------- | -------- | -------- |
| torch_ddp      | 83.4%    | 88.1%    |    1     |

## Note:
Since the `bert.ipynb` file is originally running on Google Colab, all the running log are recorded in it. However, there were some log information missing when it was downloaded from Colab. For example, all progress bars are 100% on the colab but show 0% after the download.


