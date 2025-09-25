### Prices Predictor System

An end-to-end Machine Learning project that predicts prices using a fully automated MLOps pipeline.
This repository demonstrates how to build, track, and deploy ML models with ZenML and MLflow, showcasing skills in production-grade machine learning engineering.

### What This Project Shows

1. MLOps in action – from raw data to deployed model
2. Experiment tracking & model registry with MLflow
3. Modular ZenML pipelines – scalable and reproducible
4. Automated deployment of the best performing model
5. Clean, production-ready code and configuration management

Perfect for demonstrating real-world machine learning engineering skills.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Tech Stack

Python 3.8+

ZenML – Orchestrates reproducible ML pipelines

MLflow – Experiment tracking, model registry, and deployment

Pytest – Testing framework

Docker (optional) – For containerized deployment

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 ### Project Structure
prices-predictor-system/
├── analysis/           # Exploratory data analysis & research
├── config.yaml         # Central configuration file
├── data/               # Raw datasets
├── pipelines/          # ZenML pipeline definitions
├── run_pipeline.py     # Executes the training pipeline
├── run_deployment.py   # Deploys the best model
├── sample_predict.py   # Sends a sample prediction request
├── steps/              # Pipeline steps (data, training, evaluation)
├── src/                # Core ML logic & utilities
├── tests/              # Unit and integration tests
└── requirements.txt    # Dependencies

---------------------------------------------------------------------------------------------------------------------------------------------------------

### Quick Start
1.) Clone & Setup
git clone <your-repo-url>.git
cd prices-predictor-system

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

2.) Install Dependencies
pip install --upgrade pip
pip install -r requirements.txt

3.) ZenML & MLflow Configuration
zenml integration install mlflow -y
zenml experiment-tracker register mlflow_tracker --flavor=mlflow
zenml model-deployer register mlflow --flavor=mlflow
zenml stack register local-mlflow-stack \
    -a default -o default -d mlflow -e mlflow_tracker --set

4.) Run the Pipeline & Deploy the Model

Train and evaluate the model:

python run_pipeline.py


Deploy the best model:

python run_deployment.py


Test predictions:

python sample_predict.py


Access MLflow UI (optional):

mlflow ui
# Visit http://127.0.0.1:5000

 Run Tests
pytest tests

# Key Skills Demonstrated

End-to-end ML lifecycle: data ingestion → model training → deployment

MLOps best practices: reproducible pipelines, configuration management

Experiment tracking & versioning: MLflow model registry

Automation & scalability: pipeline orchestration with ZenML

 License

MIT License – feel free to use, modify, and share.

# About This Project

This repository is designed to showcase real-world machine learning engineering skills to recruiters, hiring managers, and collaborators.
It goes beyond a simple model notebook by demonstrating production-level MLOps techniques.
