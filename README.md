# Bacterial Promoters Strength Predictor

## Project Overview
This project aims to predict RNA transcription levels in *Escherichia coli* promoters using Deep Learning (specifically, 1D Convolutional Neural Networks). It focuses on analyzing promoter sequences and classifying them based on their transcription strength (Low, Medium, or Strong). 

## Background
Gene expression is a highly regulated process, controlling RNA production in cells. The first level of control is transcription, where RNA polymerase binds to promoters in the DNA to begin RNA synthesis. This process is regulated by activators and repressors, proteins that either enhance or inhibit transcription. The goal of this project is to predict RNA levels using the DNA sequences of these promoters.

## Problem Addressed
This project is particularly useful for the scientific community, as it enhances the ability to fine-tune genetic systems by predicting how promoter sequences affect transcription levels. It could help design better synthetic biology applications, where controlling gene expression is critical.

## Methodology
1. **Data Collection**: 
   - Promoter sequences were extracted from *RegulonDB*, and gene transcription data was collected from *iModulonDB*.
   
2. **Preprocessing**:
   - Focus was placed on promoters recognized by σ70, the most common sigma factor in *E. coli*. Only genes regulated by a single promoter were considered to avoid contradictory data.

3. **Model**: 
   - A 1D Convolutional Neural Network (CNN) with an Inception-like architecture was used to classify promoter strength based on sequence data.
   - The CNN transformed sequences into binary vectors and passed them through convolutional filters to detect patterns, ultimately classifying promoters into one of three categories: Low, Medium, or Strong.

## Results
The model achieved an R² score of 0.6 despite limited data (660 promoter sequences). The accuracy was highest for medium-strength promoters, as this class was overrepresented in the dataset.

## Future Work
The project can be expanded by improving the recognition of regulatory sequences, understanding how these sequences influence gene expression, and incorporating these factors into the model to improve prediction accuracy.


## References
1. Salgado, H., et al. "RegulonDB v12.0: A Comprehensive Resource of Transcriptional Regulation in *E. coli* K-12." *Nucleic Acids Research*, 2023.
2. Rychel, K., et al. "iModulonDB: A Knowledgebase of Microbial Transcriptional Regulation Derived from Machine Learning." *Nucleic Acids Research*, 2021.
3. Tayara, H., et al. "Identification of Prokaryotic Promoters and Their Strength by Integrating Heterogeneous Features." *Genomics*, 2020.
