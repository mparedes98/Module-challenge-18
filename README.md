# Student Loan Risk Prediction with Deep Learning

## Project Overview
This project develops a deep neural network model to predict student loan repayment success for a student loan refinancing company. By accurately predicting whether a borrower will repay their loan, the company can provide more accurate interest rates and make better lending decisions.

## Background
Student loan refinancing companies face the challenge of assessing credit risk when determining appropriate interest rates for borrowers. Traditional credit scoring methods may not capture all relevant factors for student loan repayment. This project leverages deep learning techniques to create a more sophisticated prediction model using various student characteristics and academic performance indicators.

## Business Problem
The company needs to:
- Predict the likelihood of loan repayment based on student characteristics
- Provide more accurate risk assessment for interest rate determination
- Reduce default rates through better borrower evaluation
- Improve profitability through optimized lending decisions

## Dataset Features
The model uses the following features to predict credit ranking:
- **payment_history**: Historical payment behavior
- **location_parameter**: Geographic location factor
- **stem_degree_score**: STEM degree indicator and score
- **gpa_ranking**: Academic performance ranking
- **alumni_success**: Alumni success rate from institution
- **study_major_code**: Academic major classification
- **time_to_completion**: Time taken to complete degree
- **finance_workshop_score**: Financial literacy workshop performance
- **cohort_ranking**: Ranking within academic cohort
- **total_loan_score**: Overall loan risk score
- **financial_aid_score**: Financial aid dependency score

**Target Variable**: `credit_ranking` (Binary: 0 = Higher Risk, 1 = Lower Risk)

## Technical Implementation

### Model Architecture
- **Input Layer**: 11 features
- **Hidden Layer 1**: 6 neurons with ReLU activation
- **Hidden Layer 2**: 3 neurons with ReLU activation
- **Output Layer**: 1 neuron with Sigmoid activation (binary classification)
- **Total Parameters**: 97 trainable parameters

### Model Configuration
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy
- **Training Epochs**: 50
- **Data Split**: 75% training, 25% testing

### Data Preprocessing
- Feature scaling using StandardScaler
- Train-test split with stratification
- No missing values detected in dataset

## Model Performance

### Training Results
- **Final Training Accuracy**: ~76%
- **Training Loss**: ~0.49 (final epoch)
- **Test Accuracy**: 73.5%
- **Test Loss**: 0.505

### Classification Report
