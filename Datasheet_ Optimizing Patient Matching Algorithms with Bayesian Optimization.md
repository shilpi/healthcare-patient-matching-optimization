# Datasheet: Optimizing Patient Matching Algorithms with Bayesian Optimization

## Motivation

- For what purpose was the dataset created? 
  
  The Synthea dataset was created to provide realistic but synthetic patient data for healthcare research, education, and software development. It was specifically designed to enable the development and testing of healthcare applications without using real patient data, thereby avoiding privacy concerns.

- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?

  The Synthea dataset was created by the MITRE Corporation as part of their Synthetic Patient Population Simulator project. The development was funded by the Office of the National Coordinator for Health Information Technology (ONC) under the U.S. Department of Health and Human Services.

## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 

  The instances in the dataset represent synthetic patients with their demographic information, medical histories, healthcare encounters, conditions, medications, procedures, and other health-related data. For our patient matching optimization project, we primarily use the demographic attributes such as names, birth dates, addresses, and gender.

- How many instances of each type are there? 

  The Synthea sample dataset used in this project contains approximately 1,000 synthetic patient records. From these, we generated additional duplicate records with introduced errors to simulate real-world data quality issues, resulting in approximately 1,300 total records for our matching experiments.

- Is there any missing data?

  The original Synthea dataset is complete with no missing values for the core demographic fields we use (name, birth date, gender, address). However, our project deliberately introduces missing data in some fields to simulate real-world data quality issues in healthcare systems.

- Does the dataset contain data that might be considered confidential?

  No. The Synthea dataset contains only synthetic patient data that was algorithmically generated and does not represent real individuals. It was specifically designed to avoid confidentiality concerns while maintaining realistic statistical properties of healthcare data.

## Collection process

- How was the data acquired? 

  The Synthea dataset was not collected but synthetically generated using the Synthea patient simulator. This simulator uses publicly available demographic and clinical statistics to generate realistic but fictional patient records. For our project, we used the publicly available sample dataset from the Synthea project website.

- If the data is a sample of a larger subset, what was the sampling strategy? 

  The Synthea sample dataset is a smaller subset of what the Synthea generator can produce. It was created to provide a manageable yet representative sample of synthetic patient data. For our project, we used the entire sample dataset without further sampling.

- Over what time frame was the data collected?

  The Synthea data represents synthetic patients with medical histories spanning multiple years. The specific sample dataset we used was released in April 2020, but the synthetic data itself represents fictional patient records with events occurring over various timeframes.

## Preprocessing/cleaning/labeling

- Was any preprocessing/cleaning/labeling of the data done?

  For our patient matching optimization project, we performed several preprocessing steps:
  1. Selected relevant demographic fields for patient matching (name, birth date, gender, address)
  2. Created duplicate records with various types of errors (typos, missing characters, swapped characters, extra characters) to simulate real-world data quality issues
  3. Split the data into training and testing sets
  4. Generated ground truth match pairs for evaluation

- Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data?

  Yes, we preserved the original Synthea sample dataset in its raw form. All preprocessing was done on copies of the data, and the original files remain unchanged.

## Uses

- What other tasks could the dataset be used for? 

  The Synthea dataset could be used for various healthcare informatics tasks, including:
  1. Testing and development of electronic health record (EHR) systems
  2. Healthcare data integration and interoperability research
  3. Clinical decision support system development
  4. Healthcare analytics and population health studies
  5. Medical education and training

- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?

  The synthetic nature of the data means it may not capture all the nuances and complexities of real patient data. While Synthea aims to be realistic, it may not perfectly represent the distribution of errors, inconsistencies, and edge cases found in real healthcare systems. Users should be aware that models trained on this data might require adjustment when applied to real-world healthcare data.

- Are there tasks for which the dataset should not be used?

  This dataset should not be used for:
  1. Making clinical decisions about real patients
  2. Drawing epidemiological conclusions about real populations
  3. Training models that will be deployed without further validation on real data
  4. Any application where the synthetic nature of the data would lead to misleading or potentially harmful outcomes

## Distribution

- How has the dataset already been distributed? 

  The Synthea dataset is publicly available through the Synthea project website (https://synthea.mitre.org/downloads). The sample dataset we used is freely downloadable without restrictions.

- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?

  The Synthea dataset is released under the Apache License 2.0, which allows for free use, modification, and distribution, with attribution requirements.

## Maintenance

- Who maintains the dataset?

  The Synthea dataset is maintained by the MITRE Corporation as part of their ongoing Synthea project. They periodically release updated versions with improvements to the data generation algorithms and expanded clinical scenarios.
