# **Experiment Tracking in MLOps: MLFlow **

## **Introduction to MLFlow in MLOps**

An end-to-end machine learning development and bringing ML model to production is a must thing now. Hence, the MLOps field is rising.MLOps, short for Machine Learning Operations, bridges the gap between the experimental phase of machine learning and the operational stage of deployment. It encompasses practices that ensure reliable and efficient deployment and maintenance of machine learning models in production. Key aspects of MLOps include:

1. **Automation and Reproducibility**: Automating the ML pipeline ensures consistent model training, evaluation, and deployment. Reproducibility is achieved by tracking experiments, data versions, and model parameters.

2. **Continuous Integration and Delivery (CI/CD)**: Similar to software development, MLOps incorporates CI/CD practices to automate testing and deployment of machine learning models.

3. **Monitoring and Management**: Deployed models need active monitoring for performance and drift. MLOps ensures timely retraining or updates based on new data or changing conditions.

4. **Collaboration and Governance**: MLOps encourages collaboration across data scientists, engineers, and business stakeholders while enforcing governance and compliance standards.

There is a need for a platform that can be able to track and deploy ML model in a simple manner. More importantly, it is a often struggle to manage my experiment by using a simple jupyter notebook and ended up with mess files and folders. MLflow provides local and server version that you can monitor your model, but in this article, I am more interested deploying MLflow in the server.

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

<div style="text-align:center">
![MLFlow](../Images/1.png)
</div>

MLflow is available in various distributions and configurations, and one notable variant is **Charmed MLflow** by Canonical. Here's a comparison between **Charmed MLflow** and the standard **MLflow** version, with a focus on their suitability for running on Ubuntu.

### Standard MLflow Version

**Pros:**
1. **Widely Used**: Standard MLflow is a well-known and widely adopted tool for managing the machine learning lifecycle.
2. **Comprehensive Features**: Includes tracking, projects, models, and registry components, which cover the end-to-end machine learning workflow.
3. **Community Support**: Extensive community support, with many tutorials, plugins, and extensions available.
4. **Framework Compatibility**: Works with various machine learning frameworks such as TensorFlow, PyTorch, and scikit-learn.

**Cons:**
1. **Manual Setup**: Requires manual setup and configuration, which can be time-consuming, especially for complex deployments.
2. **Maintenance**: Users need to handle maintenance, updates, and scaling.

### Charmed MLflow

**Charmed MLflow** is a version of MLflow provided by Canonical, designed to work seamlessly on Ubuntu through the use of Juju, a service orchestration tool. 

**Pros:**
1. **Ease of Deployment**: Simplifies the deployment process using Juju charms, which automate the setup and management of MLflow and its dependencies.
2. **Integration**: Well-integrated with other Canonical tools and services, enhancing compatibility and performance on Ubuntu systems.
3. **Scalability**: Designed for scalability, making it easier to manage large-scale machine learning projects.
4. **Support**: Comes with professional support options from Canonical, which can be crucial for enterprise environments.

**Cons:**
1. **Learning Curve**: Requires familiarity with Juju and Canonical’s ecosystem, which might be new to some users.
2. **Less Community Content**: Compared to the standard MLflow, there might be less community-generated content and third-party plugins.

### Comparison and Suitability for Ubuntu

- **Ease of Deployment and Management**: If you are looking for a solution that is easy to deploy and manage on Ubuntu, **Charmed MLflow** is likely the better choice. The automated deployment process using Juju charms simplifies setup and scaling.
- **Community and Ecosystem**: If you prefer a tool with a large community and a plethora of resources, the **standard MLflow** might be more suitable. The broader ecosystem ensures access to a wide range of tutorials, plugins, and support from other users.
- **Support and Integration**: For enterprise environments or users who prefer professional support and tight integration with other Ubuntu tools, **Charmed MLflow** offers significant advantages.

### Which is Best on Ubuntu?

**Charmed MLflow** is typically the best choice for Ubuntu users, especially those who value ease of deployment, scalability, and integration with the Canonical ecosystem. The Juju orchestration simplifies management, and the professional support options add an extra layer of reliability.

**Standard MLflow** remains an excellent choice for those who are comfortable with manual setup and prefer leveraging the extensive community support and resources available.

### Summary

- **Charmed MLflow**: Best for users seeking ease of deployment, scalability, and professional support on Ubuntu.
- **Standard MLflow**: Ideal for those who prefer community-driven support and are comfortable with manual configurations.

Choose based on your specific needs, familiarity with Juju and the Canonical ecosystem, and the scale of your machine learning projects.

[](https://mlflow.org/docs/latest/_images/mlflow-overview.png)

MLflow provides tools to manage and track machine learning experiments. Two of the core components you might encounter when working with MLflow are `mlflow ui` and `mlflow server`. While they seem similar, they serve slightly different purposes and are used in different contexts.

### MLflow UI

**`mlflow ui`** is a command that starts a local web-based user interface for MLflow. It is primarily used for quickly visualizing the results of your experiments when you are working locally.

- **Purpose**: To provide a quick way to view and interact with your MLflow experiment logs.
- **Typical Use Case**: When you are developing or running experiments on your local machine and want to visualize the results without setting up a full server.
- **Data Storage**: Uses the default local file-based backend and artifact store unless otherwise configured.
- **Command**: 
  ```bash
  mlflow ui
  ```

- **Example Usage**:
  ```bash
  mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
  ```

### MLflow Server

**`mlflow server`** is a command to start a production-grade tracking server. It is more flexible and robust, allowing for remote access, better scalability, and integration with different backends for storing experiment data and artifacts.

- **Purpose**: To provide a scalable and robust server that can be accessed remotely, suitable for team collaborations and production environments.
- **Typical Use Case**: When you need a persistent, shared service that multiple users or systems can access, often used in enterprise environments or collaborative projects.
- **Data Storage**: Can use various backends (like MySQL, PostgreSQL, SQLite) for the metadata store and supports different artifact storage options (like S3, GCS, Azure Blob Storage).
- **Command**: 
  ```bash
  mlflow server --backend-store-uri <BACKEND_URI> --default-artifact-root <ARTIFACT_ROOT>
  ```

- **Example Usage**:
  ```bash
  mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
  ```

### Key Differences

1. **Scope and Scale**:
   - **`mlflow ui`**: Best for local development and quick, ad-hoc visualization.
   - **`mlflow server`**: Designed for production use, supporting remote access and collaboration.

2. **Configuration and Flexibility**:
   - **`mlflow ui`**: Limited configuration options, suitable for local, simple setups.
   - **`mlflow server`**: Highly configurable, allowing use of various backend stores and artifact repositories.

3. **Use Case**:
   - **`mlflow ui`**: Single user, local machine, temporary setups.
   - **`mlflow server`**: Multi-user, remote access, long-term storage, and enterprise-grade setups.

### How to Choose Between Them

- **For Local Development**: Use `mlflow ui`. It’s simple to set up and provides a quick way to visualize experiment results.
- **For Production or Team Collaboration**: Use `mlflow server`. It offers more flexibility, remote access capabilities, and can be integrated with enterprise-grade storage solutions.

### Practical Examples

**Local Development with `mlflow ui`**:
1. Start the MLflow UI:
   ```bash
   mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
   ```
2. Open your web browser and navigate to `http://localhost:5000` to see the UI.

**Production Setup with `mlflow server`**:
1. Start the MLflow server:
   ```bash
   mlflow server --backend-store-uri mysql+pymysql://user:password@host/dbname --default-artifact-root s3://my-bucket/mlflow-artifacts
   ```
2. The server is now accessible to other users or systems. They can log experiments to this server and access the UI remotely.

Choosing between `mlflow ui` and `mlflow server` depends on your specific needs. For quick local visualization and development, `mlflow ui` is sufficient. For robust, scalable, and collaborative environments, `mlflow server` is the appropriate choice. Both tools leverage the power of MLflow to track and manage machine learning experiments effectively.

## ** Guide for Week-2 task step-by-step 

### Learning objectives:

1. How to log parameters, metrics, and a model

2. The basics of the MLflow fluent API

3. How to register a model during logging

4. How to navigate to a model in the MLflow UI

5. How to load a logged model for inference

**1st step**: Get MLflow
MLflow is available on PyPI. If you don’t already have it installed on your system, you can install it with:
```bash
 pip install mlflow
```

**Step 2**: Start a Tracking UI or server
```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db
```
It starts the MLflow tracking UI with a specified SQLite database named mlflow.db located in the current directory to store experiment metadata. This command is useful for local development and allows you to view and interact with your MLflow experiments through a web interface at address: `http://localhost:5000`.
You should see the MLflow UI, where you can browse and interact with your logged experiments.

**Step 3**: Train a model and prepare metadata for logging
In Jupyter notebook of the ML code, after importing the libraries, add following:

```python
import mlflow
# Set the tracking URI to use SQLite
mlflow.set_tracking_uri("sqlite:///mlflow.db")

# Set the experiment name
mlflow.set_experiment("nyc-taxi-experiment")
```
The `mlflow.set_tracking_uri` function sets the location where MLflow will store the metadata (experiment details, metrics, parameters, etc.).

Using 'mlflow.set_experiment' function to create a new experiment or activate an existing one. Experiments are logical groupings of runs. Here, the experiment named "nyc-taxi-experiment" is activated under which your runs will be logged.

## CITATIONS
(1) MLOps with MLflow Explained — Restack. https://www.restack.io/docs/mlflow-knowledge-mlops-mlflow-guide.
(2) Tutorials and Examples — MLflow 2.13.0 documentation. https://mlflow.org/docs/latest/tutorials-and-examples/index.html.
(3) MLflow — a modern MLOps tool for data project collaboration. https://medium.com/sfu-cspmp/mlflow-a-modern-mlops-tool-for-data-project-collaboration-704ca299d9c3.
(4) MLflow | What is MLflow | MLOps now made simple using MLflow. https://www.analyticsvidhya.com/blog/2021/06/mlops-now-made-simple-using-mlflow/.
(5) An introduction to MLOps with MLflow. https://inseefrlab.github.io/formation-mlops/slides/en/index.html.
(6) en.wikipedia.org. https://en.wikipedia.org/wiki/MLOps.