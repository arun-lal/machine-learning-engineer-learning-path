# Machine Learning Options on Google Cloud
Google Cloud offers four options for building machine learning models:

1. **BigQuery ML**: Use SQL queries to create and execute machine learning models directly in BigQuery.
   - Suitable for tabular data and requires understanding SQL.
   - Ideal if your data is already in BigQuery and your problems align with pre-defined ML models.

2. **Pre-built APIs**: Leverage machine learning models already built and trained by Google.
   - Supports tabular, image, text, and video data.
   - Requires no training data and is user-friendly with low ML expertise requirements.
   - Best choice if you lack training data or ML expertise in-house.

3. **AutoML**: A no-code solution on Vertex AI, enabling custom ML model building through a point-and-click interface.
   - Supports tabular, image, text, and video data.
   - Requires your own training data, but offers simplicity and reduced coding efforts.
   - Great for developers and data scientists wanting to build custom models quickly.

4. **Custom Training**: Code your own ML environment, training, and deployment on Vertex AI Workbench.
   - Supports tabular, image, text, and video data.
   - Requires the highest ML expertise and provides full control over the ML pipeline.
   - Suitable for ML engineers and data scientists seeking complete workflow control.

## Comparison of Options

- **Data Type**: BigQuery ML supports tabular data, while the other three options support multiple data types.
- **Training Data Size**: Pre-built APIs do not require training data, while BigQuery ML and custom training need substantial data.
- **ML and Coding Expertise**: Pre-built APIs and AutoML are user-friendly with low requirements. Custom training demands high expertise, and BigQuery ML requires SQL understanding.
- **Hyperparameter Tuning**: Pre-built APIs and AutoML lack hyperparameter tuning, but BigQuery ML and custom training allow experimentation.
- **Time to Train**: Pre-built APIs use Google's pre-built models and require no training time. Custom training takes the longest, while BigQuery ML and AutoML vary depending on the project.

Choose the option that aligns with your business needs and ML expertise:
- BigQuery ML if familiar with SQL and have data in BigQuery.
- Pre-built APIs for easy-to-use, ready-made models.
- AutoML for custom models without extensive coding.
- Custom Training for full ML workflow control and customization.

In the following videos, we will explore the other three options in more detail after having already covered BigQuery ML.

## Pre-built APIs for Machine Learning

- Good Machine Learning models require extensive training data, often hundreds of thousands of records, to create a custom model.
- If you lack sufficient data, pre-built APIs can be an excellent starting point to meet your needs.
- Pre-built APIs are offered as services and can serve as building blocks to create applications without the complexity of developing your own models.
- They save time and effort by eliminating the need to build, curate, and train new datasets, allowing you to focus on making predictions.

### Popular Pre-built APIs

1. **Speech-to-Text API**: It converts audio into text for data processing.
2. **Cloud Natural Language API**: This API identifies parts of speech, such as entities, and sentiment in text.
3. **Cloud Translation API**: It converts text from one language to another.
4. **Text-to-Speech API**: This API transforms text into high-quality voice audio.
5. **Vision API**: The Vision API recognizes and analyzes content in static images.
6. **Video Intelligence API**: This API identifies motion and action within videos.

- Google has already trained these pre-built models using its vast datasets. For instance:
  - The Vision API is based on Google's image datasets.
  - The Speech-to-Text API is trained on YouTube captions.
  - The Translation API utilizes Google's neural machine translation technology.

- Google's extensive data resources and ML researchers contribute to the effectiveness of these pre-built APIs.
- Leveraging these APIs reduces the amount of work required on your part.

## AutoML: Automated Machine Learning

AutoML, short for automated machine learning, was introduced in January 2018 to simplify the time-consuming process of training and deploying ML models. It aims to automate machine learning pipelines, saving data scientists from manual tasks like tuning hyperparameters and comparing multiple models.

### Technologies behind AutoML

1. **Transfer Learning**: Similar to gathering books to create a library, transfer learning builds a knowledge base in the field. It leverages pre-trained models on similar, larger datasets to achieve state-of-the-art results with smaller datasets or less computational power.

2. **Neural Architecture Search**: This technology seeks the optimal model for a specific project, just like finding the best book in a library for learning purposes. AutoML trains and evaluates multiple models, producing an ensemble and selecting the best one.

### Benefits of AutoML

- No-Code Solution: AutoML requires minimal effort and machine learning expertise, allowing data scientists to focus on defining business problems and improving model results.

- Quick Prototyping: AutoML helps explore new datasets and identify the best features before investing in development.

### How AutoML Works

- AutoML supports four data types: image, tabular, text, and video, and solves different problems (objectives) for each type.
- For image data: Classification and object detection models are used to analyze images and return content categories or annotations.
- For tabular data: Regression, classification, and forecasting models provide numeric values, lists of categories, or predict future numeric values.
- For text data: Classification, entity extraction, and sentiment analysis models categorize text, label entities, and determine emotional opinions.
- For video data: Classification, object tracking, and action recognition models categorize shots, detect objects, and identify action moments.

### Versatility of AutoML

- AutoML can handle multiple data types and objectives, allowing it to solve diverse business problems effectively.

AutoML is a powerful tool that automates the complex aspects of machine learning, making it accessible and efficient for data scientists.

## Custom Training with Vertex AI Workbench

- Google Cloud offers several options for building machine learning models: BigQuery ML, pre-built APIs, AutoML, and custom training.
- Custom training involves coding your machine learning model using Vertex AI Workbench.
- Workbench is a single development environment that covers the entire data science workflow: exploring, training, and deploying a machine learning model with code.

### Choosing the Environment

- Before coding, decide on the environment for your ML training code: a pre-built container or a custom container.
- A pre-built container is like a fully furnished kitchen with all dependencies (appliances) and libraries (cookware), suitable for platforms like TensorFlow, Pytorch, Scikit-learn, or XGboost with Python code.
- A custom container is an empty room where you define the specific tools needed for the job.

Custom training in Vertex AI Workbench allows for a more tailored approach, giving you control over the tools and libraries used in your machine learning model.

## Google's Vertex AI: Unified Platform for Machine Learning

- Google has invested heavily in big data and AI, applying AI technologies to products like Gmail, Google Maps, Google Photos, and Google Translate.
- However, developing machine learning models and putting them into production comes with challenges, including data handling, model selection, and computing power requirements.

### Challenges Addressed by Vertex AI

1. **Production Challenges**: Scaling, monitoring, and continuous integration/continuous deployment are essential for ML models in production.
2. **Ease-of-Use Challenges**: Many tools require advanced coding skills, diverting data scientists' focus from model configuration.

### Introducing Vertex AI

- Vertex AI is a unified platform that brings all machine learning ecosystem components together, solving production and ease-of-use challenges.
- It offers one digital experience to create, deploy, and manage models at scale.

### Unified Platform Features

1. **Data Readiness**: Upload data from Cloud Storage, BigQuery, or local machines.
2. **Feature Readiness**: Create and share processed data (features) using the feature store.
3. **Training and Hyperparameter Tuning**: Experiment with different models and adjust hyperparameters.
4. **Deployment and Model Monitoring**: Set up the pipeline for automatic monitoring and continuous improvements.

### Building Machine Learning Models with Vertex AI

- Users can choose between two options: AutoML (code-less solution) or Custom Training (code-based solution).
- AutoML is user-friendly, enabling data scientists to focus on business problems.
- Custom Training offers full control over the development environment and process.

### Benefits of Vertex AI

- Four Ss:
  1. **Seamless**: Smooth user experience from data preparation to model training and production.
  2. **Scalable**: Machine Learning Operations (MLOps) automate monitoring and managing ML production, scaling storage and computing power automatically.
  3. **Sustainable**: All artifacts and features created can be reused and shared.
  4. **Speedy**: Vertex AI produces models with 80% fewer lines of code compared to competitors.

Vertex AI's unified platform provides a seamless, scalable, sustainable, and speedy solution to building and deploying machine learning models effectively.

## Google Cloud's AI Solution Portfolio

Google Cloud offers a comprehensive AI solution portfolio, organized into three layers:

1. **AI Foundation**: The bottom layer includes Google Cloud infrastructure and data.

2. **AI Development Platform**: The middle layer consists of four ML options:
   - AutoML and custom training through Vertex AI.
   - Pre-built APIs and BigQuery ML.

3. **AI Solutions**: The top layer has two groups of solutions:
   - Horizontal Solutions: Apply to any industry and address common problems.
     - Examples: Document AI for efficient document processing and CCAI for improved customer service in contact centers.
   - Vertical Solutions: Tailored to specific industries.
     - Examples: Retail Product Discovery, Google Cloud Healthcare Data Engine, and Lending DocAI for mortgage document processing.

