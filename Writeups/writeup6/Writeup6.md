#### Project Proposal

### Project Overview

## Overarching Goal
Engineer CAR T cells that produce synergistic phenotypes when expressing a
constitutively active synthetic cytokine receptor and a transcription factor 
or other payload of interest.

## Rationale
Our lab had previously generated and screened constitutively active synthetic cytokine receptors (SCRs) containing combinations of JAK/STAT signaling motifs to improve CAR T cell anti-tumor efficacy, and we observed a range of effects on CAR T cell cytotoxicity, differentiation, survival, and proliferation. Notably, these efforts revealed a trade-off between CAR T cell memory and cytotoxicity with JAK/STAT signaling modulation, limiting therapeutic efficacy as both rapid cytotoxic response and long-term memory are required for complete tumor control.
I hypothesize that combinatorial JAK/STAT signaling through SCRs can generate deviations from conventional metabolic and anti-tumor function relationships, and that co-engineering of SCRs and defined payloads will generate novel CAR T cell behaviors only accessible by combinatorial engineering.

## Specific Aims
1) Variety in CAR T cell design also produce many different cell fates with unique metabolic profiles to be effective against cancer, and optimizing these metabolic programs can enhance CAR T cell function and overcome the suppressive tumor microenvironment (TME)6,7. I hypothesize that co-engineering a nutrient transporter tailored to support the metabolic programming of an SCR CAR T cell will produce synergistic programming of cell signaling and metabolic engineering for improved CAR T cell function. I will combine expression of nutrient transporters LAT1, CAT1, and ASCT2 with SCR CAR T cells and assess for synergistic behavior through measurement of nutrient uptake, proliferation, differentiation states, and cancer cell killing performance in vitro and in vivo. This aim will reveal how variation in cell signaling and metabolism intertwine to produce high antitumor efficacy.
2) The objective of Aim  3 is to understand the phenotypes generated when SCRs are co-engineered with a transcription factor. Overexpression of transcription factors have demonstrated to enhance phenotypes in CAR T cells with therapeutic effects, such as how FOXO1 overexpression promotes a memory-like state4. I hypothesize that co-engineering SCRs driving high cytotoxicity with transcription factors that promote strong memory states will produce CAR T cells with high killing capacity and memory. To test this hypothesis, I will create a library containing combinations of SCRs, CARs, and transcription factors and perform an arrayed screen measuring cancer cell killing, proliferation, and differentiation markers. From this data, I will determine SCR-TF pairs that maximize cytotoxicity and memory-like phenotypes, establishing new principles to CAR T cell design.

### Data

## Dataset description
- Source: lab-generated flow cytometry and time course imaging data
- Size: ~250 samples with data output being cell counts, various marker expression, and confluency from imaging; all from multiple time points
- Format: CSV

## Data sutitability
- Already optimal for downstream processing or analysis

## Storage and data management
- Data does not take up large amount of storage, will primarily store and access in OneDrive but also on Google Drive for the lab and locally on computer

### Environment

## Coding environment
- Jupyter notebook

## Dependencies
- pandas
- numpy
- seaborn
- matplotlib.pyplot

## Reproducibility
- Not sure, version control?

### Pipeline

## Algorithms and methods
- My data is to observe it globally for interesting trends or outliers and then followup and filter for ones of interest, this is primarily formatting a lot of what was in the csv file
- Scalability and efficiency: the dataset size itself is not extremely large but still large enough to requrie computational methods for analysis

### Machine Learning

## Task definition
- Predict based on data from CAR T cells with combinations of receptors and payloads, predict the cancer cell killing capacity, surface marker expression level, T cell subset, and exhaustion levels of new engineered cells

## Feature representation
- Take the categories of variables (SCR, CAR, Payload) and encode into features
- Functional features: % subset, % exhausted
- Experiment features: Plate and well ID, timepoint

## Model selection
- Lasso ?

## Generalization strategy
- I will use half the samples to train, a quarter to validate, and another quarter to test

## Evaluation metrics
- R^2 on the training versus the test
