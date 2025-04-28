# Transaction Anomaly Detection
## 🎯 Overview
This project implements an intelligent system for detecting anomalous financial transactions using unsupervised machine learning techniques. By combining multiple detection methods and behavioral analysis, the system provides robust identification of suspicious transaction patterns.
This project uses Bank Transaction Dataset for Fraud Detection on [Kaggle](https://www.kaggle.com/datasets/valakhorasani/bank-transaction-dataset-for-fraud-detection/data).
## 🚀 Key Features
- Multiple anomaly detection algorithms (Isolation Forest and One-Class SVM)
- Combined scoring system with weighted risk factors
- Temporal pattern analysis
- Account balance relationship analysis
- Real-time transaction evaluation capability
- Comprehensive visualization of detection results
## 📊 Results
- Total transactions analyzed: 2,512
- Anomalies detected: 133 (5.29%)
- Model agreement rate: 74% between Isolation Forest and One-Class SVM
- High-value transaction detection accuracy: 95.6%
## 🔧 Installation & Setup
1. Clone the repository:
   ```
   git clone https://github.com/ghsaberr/transaction-anomaly-detection
   cd transaction-anomaly-detection
   ```

2. Create a virtual environment (recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
## 📈 Model Components
### 1. Isolation Forest
- Purpose: Isolates anomalies by recursively partitioning data
- Key Parameter: contamination=0.1 (expects 10% anomalous transactions)
- Advantages:
    - Fast training and prediction
    - Handles high-dimensional data well
    - Provides feature importance scores
### 2. One-Class SVM
- Purpose: Learns a decision boundary around normal data
- Key Parameter: nu=0.1 (controls boundary strictness)
- Advantages:
    - Effective at finding global anomalies
    - Works well with non-linear patterns
    - Robust decision boundary
### 3. Combined Scoring System
Features weighted risk factors including:
- Machine learning model predictions
- High amount outliers
- Unusual transaction hours
- Extended periods of inactivity
- Unusual transaction frequency
## 🔍 Key Findings
1. ML models detected more sophisticated patterns than simple threshold-based methods
2. Strong agreement between different detection methods validates the approach
3. Combined scoring system provides more selective and accurate detection
4. Temporal and behavioral patterns improve detection accuracy
## 🔄 Future Improvements
- Implement real-time model adaptation
- Add more behavioral patterns
- Develop active learning system
- Include geographic analysis
- Add merchant category analysis
- Implement network-based detection