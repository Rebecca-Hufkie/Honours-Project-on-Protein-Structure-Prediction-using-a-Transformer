# Honours-Project-on-Protein-Structure-Prediction-using-a-Transformer

**Title: Optimising Transformers for Protein Structure Prediction and Visualisation**

## Overview
This project explores transformer-based architectures for sidechain angle prediction to construct the 3D structure of a protein using the CASP12 dataset available from SidechainNet. 

This repository contains the full implementation and experiments developed during this honours project. This system implements a transformer model used for sidechain angle prediction.
Four models were trained: 
- two baselines
- two optimised
  
Each with the different input configurations:
- sequence-only
- sequence combined with additional structural features (secondary structure, backbone angles, evolutionary information)

## Instalaltion
The following installs are required:
- openmm
- sidechainnet
- pytorch_lightning

## Dataset
This project uses a dataset from the SidechainNet framework. The dataset is loaded and presplit into training, validation and testing.
The dataset contained angles, secondary structures, evolutionary information, 3D coordinates and protein sequences.

## Model Architecture
The model is an encoder-only Transformer architecture that outputs the sine and cosine angles for each sidechain angle

## References
King, Jonathan Edward and Koes, David Ryan. SidechainNet: An all-atom protein structure dataset for machine learning. Proteins: Structure, Function, and Bioinformatics, 2021, doi:10.1002/prot.26169
Vaswani, A. et al. Attention is All You Need. NeurIPS, 2017.
