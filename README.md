```markdown
# 🎓 IntelliPredict: Scalable ML System for Student Performance Forecasting

This project is a complete Machine Learning pipeline built to predict student academic performance based on various features such as study time, past failures, absences, etc. It is designed for production readiness with modular architecture, error handling, logging, model evaluation, and multiple deployment pipelines.

---

## 🚀 Features

- End-to-end ML pipeline: data ingestion ➝ transformation ➝ training ➝ evaluation ➝ prediction
- Fully modular and object-oriented codebase
- Exception handling and logging integrated into every component
- Hyperparameter tuning using GridSearchCV
- Flask-based prediction API
- CI/CD deployment using GitHub Actions, AWS, and Azure

---

## 📊 Problem Statement

To predict final student performance using input attributes collected during their academic sessions. The goal is to help educational institutions proactively support students who may be at risk of poor outcomes.

---

## 🧠 Key Data Structures Used

- **Dictionary & JSON:** For configuration management and model metadata  
- **Pandas DataFrames:** For structured data processing  
- **Pipeline (scikit-learn):** For transforming data and building model workflows  
- **Custom Classes & Objects:** For components like DataIngestion, DataTransformation, and ModelTrainer  
- **Exception Classes:** For custom error handling across the project  
- **Logging Handlers:** To trace pipeline execution and errors  

---

## 🧪 Testing

- Unit testing implemented for core components (data ingestion, transformation, training)
- Logging and exception flow validated with intentional edge cases
- Model predictions tested on real-world student data to evaluate consistency

---

## 🛠️ Tech Stack

- **Languages:** Python 3.8+  
- **Libraries:** pandas, numpy, scikit-learn, seaborn, matplotlib, joblib  
- **Web Framework:** Flask  
- **Environment:** Conda / venv  
- **Deployment:** Docker, GitHub Actions, AWS EC2, Azure Web App  
- **CI/CD:** GitHub Workflows  
- **Others:** Logging, Exception Handling, GridSearchCV  

---

## ⚙️ Machine Learning Workflow

### 🔹 Data Ingestion
- Loads CSV dataset
- Splits into train/test sets
- Stores processed files into `artifacts/` directory

### 🔹 Data Transformation
- Handles missing data and encoding
- Applies scaling using scikit-learn pipelines
- Saves transformed objects for reuse

### 🔹 Model Training
- Trains multiple models and selects best via GridSearchCV
- Saves trained model artifacts

### 🔹 Model Evaluation
- Evaluates using metrics like RMSE, MAE, and R² score
- Compares current vs previous models

### 🔹 Prediction Pipeline
- Loads saved model and transformers
- Accepts user input via Flask app
- Returns performance prediction instantly

---

## 🚀 Deployment Methods

### ✅ GitHub Actions (CI/CD)
- Automates build, test, and deployment processes on every push
- Ensures code quality and reproducibility

### ✅ AWS EC2
- Docker-based deployment of Flask application
- Supports scaling and remote access

### ✅ Azure Web App
- Integrated deployment via GitHub Actions
- Supports automatic redeployment on code changes

---

## 💻 How to Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/mlproject.git
cd mlproject
````

### 2. Create and activate virtual environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Train the model

```bash
python src/pipeline/training_pipeline.py
```

### 5. Launch the Flask web app

```bash
python app.py
```

Visit `http://127.0.0.1:5000` in your browser to use the prediction interface.

---

## 🐳 Run with Docker

```bash
docker build -t student-performance-app .
docker run -p 5000:5000 student-performance-app
```

---

## 📌 Future Enhancements

* Add support for real-time analytics dashboard
* Feature importance visualizations using SHAP or LIME
* Notification system for at-risk students via email or SMS

---

## 👩‍💻 Author

**Harshita Lalwani**
Third-Year Computer Science Student | Machine Learning Enthusiast
[LinkedIn](https://www.linkedin.com/in/harshitalalwani) 

---

## 📜 License

This project is licensed under the MIT License.

```

