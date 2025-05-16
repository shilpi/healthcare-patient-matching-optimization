# Optimizing Patient Matching for Healthcare Interoperability

## Project Overview

This project applies Bayesian optimization techniques to improve patient matching in healthcare systems. Patient matching is a critical challenge in healthcare interoperability, as it determines whether records from different systems belong to the same patient. Incorrect matches can lead to medical errors, while missed matches result in fragmented care.

## Non-Technical Summary

When you visit different healthcare providers, your medical records may be stored in separate systems. For these systems to share information effectively, they need to correctly identify which records belong to the same person. This is challenging because names might be spelled differently, addresses change, and data entry errors occur.

Our solution uses an advanced technique called Bayesian optimization to find the best settings for patient matching algorithms. Rather than manually adjusting settings through trial and error, our approach automatically discovers which patient attributes (like name, birth date, or address) should be given more importance when comparing records, and how similar records need to be before we consider them a match.

Using synthetic patient data that mimics real-world healthcare records, our optimized matching system achieved 90% accuracy in correctly linking patient records. This represents a significant improvement over standard approaches and could help healthcare organizations provide better coordinated care by ensuring complete patient information is available to providers.

## Key Features

- Bayesian optimization framework for tuning patient matching parameters
- Configurable field weights and similarity thresholds
- Multiple string comparison methods for different demographic fields
- Comprehensive evaluation metrics (precision, recall, F1 score)
- Visualization of optimization progress and results

## Repository Structure

- `code/`: Contains the Jupyter Notebook with implementation and results
- `data/`: Contains the synthetic patient data used for the project
- `data_sheet.md`: Detailed information about the dataset
- `model_card.md`: Documentation of the model, its intended use, and limitations
- `README.md`: This file, with project overview and instructions

## Getting Started

1. Clone this repository
2. Install required dependencies: `pip install -r requirements.txt`
3. Run the Jupyter Notebook: `jupyter notebook code/patient_matching_optimization.ipynb`

## Results

Our optimized patient matching algorithm achieved:
- Precision: 92%
- Recall: 88%
- F1 Score: 90%

The most important fields for accurate matching were found to be last name, first name, and birth date, with optimal weights determined through Bayesian optimization.

## Future Work

- Extend the approach to handle more complex matching scenarios
- Incorporate additional data sources and identifiers
- Develop an interactive tool for healthcare organizations to optimize their specific matching algorithms
- Explore federated matching approaches for cross-organizational patient identification

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- MITRE Corporation for the Synthea synthetic patient dataset
- Imperial College London Professional Certificate in Machine Learning and AI program
