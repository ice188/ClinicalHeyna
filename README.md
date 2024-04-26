# clinicalHeyna

This repository contains the code to pretrain and fine-tune clinicalHeyna model on MIMIC-III dataset for hospital readmission task.

## Instruction 
1. generate pretraining and fine-tuning data from  MIMIC-III in the same fashion as [ClinicalBERT](https://arxiv.org/abs/1904.05342)
2. load Heyna checkpoint trained on 150 billion tokens on [The Pile](https://pile.eleuther.ai/)
3. pre-train on clinical texts
4. fine-tune on hospital readmission task (including early notes and discharge notes)
5. evaluate performance on readmission test set

Steps 2 to 5 are contained in the colab notebook code/clinicalHeyna.ipynb.
