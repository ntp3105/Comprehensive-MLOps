# **Experiment Tracking in MLOps: MLFlow **

## **Introduction to MLOps**
MLOps, short for Machine Learning Operations, bridges the gap between the experimental phase of machine learning and the operational stage of deployment. It encompasses practices that ensure reliable and efficient deployment and maintenance of machine learning models in production. Key aspects of MLOps include:

1. **Automation and Reproducibility**: Automating the ML pipeline ensures consistent model training, evaluation, and deployment. Reproducibility is achieved by tracking experiments, data versions, and model parameters.

2. **Continuous Integration and Delivery (CI/CD)**: Similar to software development, MLOps incorporates CI/CD practices to automate testing and deployment of machine learning models.

3. **Monitoring and Management**: Deployed models need active monitoring for performance and drift. MLOps ensures timely retraining or updates based on new data or changing conditions.

4. **Collaboration and Governance**: MLOps encourages collaboration across data scientists, engineers, and business stakeholders while enforcing governance and compliance standards.

## **What is MLflow?**
MLFlow, an open-source platform, plays a crucial role in MLOps. It is developed to assist machine learning practitioners and teams in handling the complexities of the machine learning proces, assist them to navigate the intricate maze of model development, deployment, and management. Here's how:

- **Unified Platform**: MLFlow provides a unified platform to manage the entire ML lifecycle, streamlining otherwise cumbersome logging, organization, and lineage concerns that are unique to model development. This focus allows you to ensure that your ML projects are robust, transparent, and ready for real-world challenges.

- **Automation and Scalability**: It enables automation, reproducibility, and scalability in machine learning projects.

## **Core Components of MLflow**
MLflow, at its core, provides a suite of tools aimed at simplifying the ML workflow. MLflow’s expansive functionalities are rooted in several foundational components:

1. **[Tracking](https://mlflow.org/docs/latest/tracking.html#tracking)**: MLflow Tracking provides both an API and UI dedicated to the logging of parameters, code versions, metrics, and artifacts during the ML process. This centralized repository captures details such as parameters, metrics, artifacts, data, and environment configurations, giving teams insight into their models’ evolution over time. Whether working in standalone scripts, notebooks, or other environments, Tracking facilitates the logging of results either to local files or a server, making it easier to compare multiple runs across different users.

2. **[Model Registry](https://mlflow.org/docs/latest/model-registry.html#registry)**: A systematic approach to model management, the Model Registry assists in handling different versions of models, discerning their current state, and ensuring smooth productionization. It offers a centralized model store, APIs, and UI to collaboratively manage an MLflow Model’s full lifecycle, including model lineage, versioning, aliasing, tagging, and annotations.

3. **[MLflow Deployments for LLMs](https://mlflow.org/docs/latest/llms/deployments/index.html#deployments)**: This server, equipped with a set of standardized APIs, streamlines access to both SaaS and OSS LLM models. It serves as a unified interface, bolstering security through authenticated access, and offers a common set of APIs for prominent LLMs.

4. **[Evaluate**](https://mlflow.org/docs/latest/models.html#model-evaluation): Designed for in-depth model analysis, this set of tools facilitates objective model comparison, be it traditional ML algorithms or cutting-edge LLMs.

5. **[Prompt Engineering UI](https://mlflow.org/docs/latest/llms/prompt-engineering/index.html#prompt-engineering)**: A dedicated environment for prompt engineering, this UI-centric component provides a space for prompt experimentation, refinement, evaluation, testing, and deployment.

6. **[Recipes](https://mlflow.org/docs/latest/recipes.html#recipes)**: Serving as a guide for structuring ML projects, Recipes, while offering recommendations, are focused on ensuring functional end results optimized for real-world deployment scenarios.

7. **[Projects](https://mlflow.org/docs/latest/projects.html#projects)**: MLflow Projects standardize the packaging of ML code, workflows, and artifacts, akin to an executable. Each project, be it a directory with code or a Git repository, employs a descriptor or convention to define its dependencies and execution method.

By integrating these core components, MLflow offers an end-to-end platform, ensuring efficiency, consistency, and traceability throughout the ML lifecycle.

## **Applications and Examples**
MLFlow can be applied in various scenarios:

1. **Experiment Tracking**: Log and query experiments, including code, data, configuration, and results. This helps data scientists keep track of their work and compare different approaches.

2. **Model Packaging and Deployment**: MLFlow's Projects feature allows packaging reproducible runs on any platform. Models can be deployed to diverse deployment tools using the Models component.

3. **Model Registry**: The Registry serves as a central model store, managing the full lifecycle of an MLflow Model. It facilitates collaboration and version control.

[](https://mlflow.org/docs/latest/_images/mlflow-overview.png)


## ** Guide for Week-2 task step-by-step 

### Learning objectives:

1. How to log parameters, metrics, and a model

2. The basics of the MLflow fluent API

3. How to register a model during logging

4. How to navigate to a model in the MLflow UI

5. How to load a logged model for inference


## **Example Use Case**
Suppose we want to optimize hyperparameters for a machine learning model. We can use MLFlow to:
1. Run a hyperparameter sweep.
2. Compare runs using the MLFlow UI.
3. Select the best model.
4. Deploy the model to a REST API or build a container image for cloud deployment.



Source: Conversation with Bing, 25/5/2024
(1) MLOps with MLflow Explained — Restack. https://www.restack.io/docs/mlflow-knowledge-mlops-mlflow-guide.
(2) Tutorials and Examples — MLflow 2.13.0 documentation. https://mlflow.org/docs/latest/tutorials-and-examples/index.html.
(3) MLflow — a modern MLOps tool for data project collaboration. https://medium.com/sfu-cspmp/mlflow-a-modern-mlops-tool-for-data-project-collaboration-704ca299d9c3.
(4) MLflow | What is MLflow | MLOps now made simple using MLflow. https://www.analyticsvidhya.com/blog/2021/06/mlops-now-made-simple-using-mlflow/.
(5) An introduction to MLOps with MLflow. https://inseefrlab.github.io/formation-mlops/slides/en/index.html.
(6) en.wikipedia.org. https://en.wikipedia.org/wiki/MLOps.