# ClinicalHeyna: Hospital Readmission Prediction with Large Convolution Language Model

This repository contains the code to generate a clinicalHeyna model ([report](tmp_link)) by fine-tuning the [Heyna base model](https://arxiv.org/abs/2302.10866) on MIMIC-III dataset for hospital readmission task.

## Experiment Steps
1. Generate pretraining and fine-tuning data from  MIMIC-III in the same fashion as [ClinicalBERT](https://arxiv.org/abs/1904.05342)
2. Load Heyna checkpoint trained on 150 billion tokens on The Pile by downloading heyna_small_150b_tok.ckpt and heyna_small_150b.yaml from [here](https://github.com/HazyResearch/safari)
3. Pre-train on clinical texts
4. Fine-tune on hospital readmission task (including early notes and discharge notes)
5. Evaluate performance on readmission test set

Step 1 is in the notebook code/generateDatasets.ipynb. 

Steps 3 to 5 are contained in the the colab notebook code/clinicalHeyna.ipynb, which was adapted from the notebook for [HeynaDNA](https://github.com/HazyResearch/hyena-dna).
