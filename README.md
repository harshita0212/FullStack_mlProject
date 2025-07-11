```markdown
# 🎓 IntelliPredict: Scalable ML System for Student Performance Forecasting

This project implements a complete **Machine Learning lifecycle** to predict student academic performance using various attributes. It follows a robust and scalable architecture, including data pipelines, model training, evaluation, exception handling, logging, and CI/CD-based deployment.

---

## 🚀 Features

- End-to-end ML pipeline: Data ingestion ➝ transformation ➝ training ➝ evaluation ➝ prediction
- Modular and production-grade code structure
- Custom logging and exception handling mechanisms
- Model hyperparameter tuning using **GridSearchCV**
- Integrated prediction API using **Flask**
- Automated deployment using **GitHub Actions** and **CI/CD pipelines**

---

## 📊 Problem Statement

The goal is to predict the final performance score of students based on features like study time, failures, absences, parental education level, and more. The model is trained to help educational institutions better support students at risk of underperformance.

---

## 📁 Project Structure

```

mlproject/
│
├── src/
│   ├── components/         # Core modules like data ingestion, transformation, training
│   ├── pipeline/           # Training and prediction pipelines
│   ├── exception.py        # Custom exception handling
│   ├── logger.py           # Logging system
│   └── utils.py            # Utility functions
│
├── artifacts/              # Generated datasets and model files
├── templates/              # HTML templates for Flask web app
├── app.py                  # Flask web app for prediction
├── requirements.txt        # Project dependencies
├── setup.py                # Installation and packaging
├── Dockerfile              # Docker config for containerization
├── .github/workflows/      # CI/CD pipeline configurations
└── README.md               # Project documentation

````

---

## 🔧 Tech Stack

- **Programming Language:** Python 3.8+
- **Data Processing:** pandas, numpy, scikit-learn
- **Modeling:** scikit-learn (Linear Regression, Decision Tree, Random Forest)
- **Visualization:** seaborn, matplotlib (for EDA)
- **Web Framework:** Flask
- **Packaging & Deployment:** Docker, GitHub Actions, AWS, Azure Web App
- **Build Tools:** CMake, make (for CI/CD if needed)
- **Environment:** Conda/venv, requirements.txt
- **Others:** Logging, Custom Exceptions, GridSearchCV for tuning

---

## ⚙️ ML Pipeline Overview

### 1. **Data Ingestion**
- Loads dataset from CSV
- Splits into train/test sets
- Saves processed datasets to `artifacts/`

### 2. **Data Transformation**
- Handles missing values
- Encodes categorical variables
- Standardizes features using pipelines

### 3. **Model Training**
- Trains multiple models and selects the best one using GridSearchCV
- Saves the final trained model

### 4. **Model Evaluation**
- Evaluates model performance on test data
- Outputs RMSE, R², MAE

### 5. **Prediction Pipeline**
- Loads saved model
- Accepts input via Flask UI
- Returns prediction results

---

## 🧪 Testing

- Logging and Exception Handling modules tested independently
- Data ingestion and transformation stages tested via unit tests
- Test script available to validate model pipeline

---

## 🚀 Deployment Methods

### ✅ GitHub Actions (CI/CD)
- Automatically builds and tests the application on push
- Deploys to cloud platforms based on configuration

### ✅ AWS Deployment
- Uses EC2 / S3 for hosting and storing models
- CI/CD integrated through GitHub Actions

### ✅ Azure Web App Deployment
- Deploys Flask app to Azure using GitHub workflows
- Scalable deployment with automatic triggers

---

## 🔍 How to Run the Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/mlproject.git
cd mlproject
````

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Train the Model

```bash
python src/pipeline/training_pipeline.py
```

### 5. Run Flask App

```bash
python app.py
```

Visit `http://127.0.0.1:5000` to access the prediction web app.

---

## 📦 Docker Support

To run using Docker:

```bash
docker build -t student-performance-app .
docker run -p 5000:5000 student-performance-app
```

---

## 📌 Future Enhancements

* Add support for real-time student dashboards
* Integrate feature importance visualizations
* Enable SMS/email alerts for students at risk

---

## 👩‍💻 Author

**Harshita Lalwani**
Third-Year CS Student | Python & Data Science Enthusiast
[LinkedIn](https://www.linkedin.com/in/harshitalalwani) 

---

## 📜 License

This project is licensed under the MIT License.

```
