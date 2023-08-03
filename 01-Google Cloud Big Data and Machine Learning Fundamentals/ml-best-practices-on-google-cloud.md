# Best Practices for Implementing Machine Learning on Google Cloud

## Overview
This document introduces best practices for implementing machine learning (ML) on Google Cloud, focusing on custom-trained models based on your data and code. It covers the following stages in the ML workflow:

1. ML Development
2. Data Processing
3. Operationalized Training
4. Model Deployment and Serving
5. ML Workflow Orchestration
6. Artifact Organization
7. Model Monitoring

These best practices aim to help data scientists and ML architects understand the scope of activities involved in using ML on Google Cloud and plan accordingly.

## ML Development
- Use Vertex AI Workbench notebooks for experimentation and development.
- Create a notebook instance for each team member to treat it as a virtual workspace.
- Store ML resources and artifacts based on your corporate policy.
- Utilize Vertex AI SDK for Python to work seamlessly with various ML frameworks.

## Data Processing
- Use BigQuery to store structured and semi-structured data, following recommended project structure.
- Store image, video, audio, and unstructured data on Cloud Storage in large container formats.
- Use Vertex AI Data Labeling for unstructured data, using in-house labelers or hiring your own.
- When training with structured data, explore existing features in Vertex AI Feature Store before creating new ones.
- Regularly compute new feature values and ingest them into Vertex AI Feature Store.

## Operationalized Training
- Run your code in a managed service like Vertex AI Training Service or Pipelines.
- Operationalize job execution with training pipelines to automate training jobs.
- Always use training checkpoints to save the current state of your experiments.
- Store model artifacts in Cloud Storage for serving purposes.
- Regularly compute new feature values for online serving scenarios.

## Model Deployment and Serving
- Choose appropriate hardware for model deployment based on model types (CPU, GPU, etc.).
- Plan how you'll pass inputs to the model for batch or online prediction.
- Turn on automatic scaling for online prediction with a minimum of two nodes for high availability.

## ML Workflow Orchestration
- Use Vertex AI Pipelines to orchestrate the ML workflow, supporting DAGs from various frameworks.
- Consider using Kubeflow Pipelines SDK for flexible pipeline construction with Google Cloud Pipeline Components.

## Artifact Organization
- Organize ML model artifacts in different storage locations, including Vertex AI Workbench, Model Registry, Artifact Registry, and more.
- Use source control repositories to version control ML pipelines and custom components.

## Model Monitoring
- Use skew and drift detection to monitor data deviations from training data.
- Fine-tune alert thresholds for skew and drift detection based on use case and expertise.
- Utilize feature attributions from Vertex Explainable AI to detect data drift or skew in complex feature types.

These best practices will help ensure smooth implementation of machine learning on Google Cloud and facilitate continuous improvement in model performance and efficiency.

