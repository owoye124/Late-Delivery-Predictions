# Late Delivery Prediction Project

Welcome to the Late Delivery Prediction project repository! This project is focused on developing an AI-powered solution to predict late deliveries with a high accuracy of at least 95%. Late deliveries can significantly impact customer satisfaction and operational efficiency, making predictive solutions vital for optimizing supply chain management.

## Project Overview

In the realm of supply chain management, timely deliveries are crucial for maintaining customer satisfaction and operational efficiency. Delays in deliveries can lead to increased costs, lost sales, and damaged client relationships. The objective of this project is to develop a machine learning model that accurately predicts the risk of late deliveries in the supply chain. By leveraging historical delivery data, including factors such as order volume, shipping distance, carrier performance, and weather conditions, the model identifies patterns and indicators that contribute to delivery delays.

## Key Analytical Insights
- What is the average difference between scheduled and actual shipping days?
- How many orders are delivered late or canceled, and what percentage of total orders does this represent?
- Which shipping modes are associated with the fastest delivery times?
- What is the average profit per order, and how does it vary by customer segment or product category?
- Which products or categories yield the highest profit margins?
- Which regions or cities have the highest sales and profit?
- Are there specific areas with higher late delivery risks?

## Steps Taken to Achieve the Solution

### 1. **Data Collection**
   - Utilized the `DataCoSupplyChainDataset.csv` dataset containing historical delivery records, including features such as:
     - Delivery dates and times
     - Order details (e.g., product type, quantity, priority)
     - Customer information (e.g., location, demographics)
     - Carrier performance metrics
     - Weather and traffic data

### 2. **Exploratory Data Analysis (EDA)**
   - Conducted EDA to uncover patterns and trends in the data.
   - Addressed questions such as average delivery times, profit margins, and regional risks.
   - Visualized data using tools like `seaborn`, `matplotlib`, and `plotly`.

### 3. **Data Preprocessing**
   - Cleaned and prepared the dataset:
     - Removed duplicates and handled missing values.
     - Normalized and scaled numerical features.
     - Encoded categorical features using one-hot encoding and label encoding.
   - Engineered new features, such as delivery urgency and distance metrics.

### 4. **Feature Selection**
   - Identified the most relevant features using techniques like:
     - Correlation analysis
     - Feature importance from tree-based models
     - Recursive feature elimination (RFE)

### 5. **Model Development**
   - Split the data into training and testing sets (80/20 split).
   - Experimented with various machine learning models, including:
     - Random Forest
     - Gradient Boosting (XGBoost, LightGBM)
     - Support Vector Machines (SVM)
     - Neural Networks
   - Tuned hyperparameters using grid search and Bayesian optimization to maximize performance.

### 6. **Model Evaluation**
   - Evaluated model performance using metrics such as:
     - Accuracy
     - Precision
     - Recall
     - F1-score
     - Area Under the ROC Curve (AUC-ROC)
   - Achieved a final accuracy of 95% on the testing set.

### 7. **Model Deployment**
   - Saved the final model as `LateDeliveryModel.pkl`.
   - Provided scripts for deployment using Flask for real-time predictions.

## How to Use This Repository

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-username/late-delivery-prediction.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the preprocessing and training scripts:
   ```bash
   python preprocess_data.py
   python train_model.py
   ```
4. Use the deployed model for predictions:
   ```bash
   python app.py
   ```

## Project Structure
```
.
├── data/                  # Dataset files
├── notebooks/             # Jupyter notebooks for EDA and experiments
├── scripts/               # Scripts for preprocessing and training
├── models/                # Saved models
├── app.py                 # Deployment script
├── requirements.txt       # Python dependencies
├── README.md              # Project description
```

## Results
The final model achieved:
- **99% Accuracy** on the test set
- High precision and recall, ensuring reliability for critical use cases.

## Future Improvements
- Incorporate real-time data streams for dynamic predictions.
- Explore advanced deep learning architectures for further accuracy improvements.
- Enhance model explainability for better stakeholder understanding.

