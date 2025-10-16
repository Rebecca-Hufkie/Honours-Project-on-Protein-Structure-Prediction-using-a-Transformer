# Honours-Project-on-Protein-Structure-Prediction-using-a-Transformer

**Title: Optimising Transformers for Protein Structure Prediction and Visualisation**

## Abstract
Proteins are seen as life's building blocks and play vital roles in the cell, such as transport, tissue formation, and immune responses. Proteins comprise amino acids with unique chemical properties and behaviour determined by their sidechain group. Predicting a protein's 3D structure from its amino acid sequence is one of the most critical challenges in bioinformatics. While experimental methods have yielded successful results, they can be expensive and slow. Traditional machine learning methods are faster but do not scale well to extensive protein data. Recent progress in deep learning, specifically transformer-based architectures, has shown success in addressing these challenges. 

This study presents a protein structure prediction system that implements a transformer that predicts sidechain angles and reconstructs the 3D structure of a protein. This study involved training the model on two different input configurations: one using only the amino acid sequence and the second incorporating additional structural features. 

The optimised additional features model achieved the best performance with a Root Mean Squared Error (RMSE) of 0.244 and a Root Mean Squared Deviation (RMSD) of 1.41 Angstroms. These results show that structural features are beneficial to the model's learning and prediction accuracy. The proposed system contributes to more precise sidechain angle prediction, to assist in drug design and potential disease treatments.

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
