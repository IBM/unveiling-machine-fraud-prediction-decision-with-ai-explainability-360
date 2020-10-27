# Unveiling-machine-fraud-prediction-decision-with-ai-explainability-360
"' '"

Imagine a scenario, you visit a bank for a loan of 1 million dollars. The Loan officer is aided by an AI-powered system which predicts or recommends if you are eligible for a loan or not and how much. The AI system recommended that you are not eligible for loan. Here are couple of questions to think upon, 

- Will you as a customer be satisfied with the service?
- Won't you want a proper justification for the decision taken by AI?
- Won't the loan officer double check the decision taken by AI and for that he or she would want to know the underlying mechanism of the AI model?
- Should the banks completely trust and rely on AI-powered systems?

After pondering upon these questions, you will agree that It’s not enough to make predictions. Sometimes, you need to generate a deep understanding. Just because you model something doesn’t mean you really know how it works. 

There are multiple reasons why we need to understand the underlying mechanism of the Machine learning Models -

- Human Readability: Explainable AI gives the reasoning behind certain decisions, and that can both increase transparency and help offer better business understanding.
- Bias Mitigation.
- Justifiability.
- Interpretability.

![](https://github.com/IBM/unveiling-machine-fraud-prediction-decision-with-ai-explainability-360/blob/main/doc/source/images/AIX360_1.png)

 [**AI Explainability 360](http://aix360.mybluemix.net/)[**[https://aix360.mybluemix.net/](https://aix360.mybluemix.net/)**],** a comprehensive open source toolkit of state-of-the-art algorithms that support the interpretability and explainability of machine learning models. 

This Code Pattern highlights the use of the AI explainability 360 toolkits to demystify the decisions taken by the machine learning model to gain better insights and explainability which not only help the policy-makers, data scientists to develop trusted explainable AI applications but also the general public for transparency and allowing them to gain insight into the machine’s decision-making process. Understanding behind the scenes is essential to fostering trust and confidence in AI systems.

To demonstrate the use of the AI Explainability 360 Toolkit, we are using the existing Fraud Detection Code Pattern showcasing, explaining, and also guide the practitioner on choosing an appropriate explanation method or algorithm depending upon the type of customer(Data Scientist, General Public, SME, Policy Maker) that needs an explanation of the model. 

This Code Pattern will also demonstrate the use of ART(Adversarial Robustness 360 Toolkit) to defend and evaluate Machine Learning models and applications against the adversarial threats of Evasion, Poisoning, Extraction, and Inference.

![https://www.ibm.com/blogs/research/wp-content/uploads/2019/08/Screen-Shot-2019-08-06-at-11.44.36-PM-1024x636.png](https://www.ibm.com/blogs/research/wp-content/uploads/2019/08/Screen-Shot-2019-08-06-at-11.44.36-PM-1024x636.png)

**No single approach to explaining algorithms**

Currently, AI explainability 360 toolkit provides eight state-of-the-art explainability algorithms that can add transparency throughout AI systems. Depending on the requirement and subjected to the problem statement you can choose them appropriately. The algorithms are explained in detail on this [link.](https://aix360.mybluemix.net/))

![](https://github.com/IBM/unveiling-machine-fraud-prediction-decision-with-ai-explainability-360/blob/main/doc/source/images/aix360_2.png)

In this Code Pattern, we will demonstrate the working of the three explainability Algorithms:

1. Contrastive Explanations Method (CEM) algorithm available in AI Explainability 360.
2. AI Explainability 360—ProtoDash—works with an existing predictive model to show how the customer compares to others who have similar profiles and had similar repayment records to the model's prediction for the current customer, which helps to evaluate and predict the applicant’s risk. Based on the model’s prediction and the explanation for how it came to that recommendation, the Loan Officer can make a more informed decision.
3. Generalized Linear Rule Model (GLRM) algorithm in the AI Explainability 360 Toolkit, which provides an enhanced level of explainability  to a Data Scientist if the model can be deployed or not.
4. Robustness : 

Architecture: 

![](https://github.com/IBM/unveiling-machine-fraud-prediction-decision-with-ai-explainability-360/blob/main/doc/source/images/AIX360_Arch.png)

Flow:

1. Log in to Watson Studio powered by spark, initiate Cloud Object Storage, and  create a project.
2. Upload the .csv data file to Object Storage.
3. Load the Data File in Watson Studio Notebook.
4. Install AI Explainability 360 Toolkit and Adversarial Robustness Toolbox in the Watson Studio Notebook.
5. Visualization for explainability and interpretability of AI Model for the three different types of Users.

## Included components

* [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.

* [IBM Auto AI](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-overview.html):The AutoAI graphical tool in Watson Studio automatically analyzes your data and generates candidate model pipelines customized for your predictive modeling problem.  

* [IBM Cloud Object Storage](https://console.bluemix.net/catalog/services/cloud-object-storage): An IBM Cloud service that provides an unstructured cloud data store to build and deliver cost effective apps and services with high reliability and fast speed to market. This code pattern uses Cloud Object Storage.


## Featured technologies

* [Artificial Intelligence](https://developer.ibm.com/technologies/artificial-intelligence/): Any system which can mimic cognitive functions that humans associate with the human mind, such as learning and problem solving.
* [Data Science](https://developer.ibm.com/code/technologies/data-science/): Systems and scientific methods to analyze structured and unstructured data in order to extract knowledge and insights.
* [Analytics](https://developer.ibm.com/code/technologies/analytics/): Analytics delivers the value of data for the enterprise.
* [Python](https://www.python.org/): Python is a programming language that lets you work more quickly and integrate your systems more effectively.

Steps: 

1. [Create an account with IBM Cloud](#1-create-an-account-with-ibm-cloud)
1. [Create a new Watson Studio project](#2-create-a-new-watson-studio-project)
1. [Add Data](#3-add-data)
1. [Add Asset as Auto AI](#4-add-asset-as-auto-ai)
1. [Create and define experiment](#5-create-and-define-experiment)
1. [Import the csv file](#6-import-the-csv-file)
1. [Run experiment](#7-run-experiment)
1. [Analyze results](#8-analyze-results)
1. [Deploy to Cloud](#9-deploy-to-cloud)
1. [Model testing](#10-model-testing)


## 1. Create an account with IBM Cloud

Sign up for IBM [**Cloud**](https://console.bluemix.net/). By clicking on create a free account you will get 30 days trial account.

## 2. Create a new Watson Studio project

Sign up for IBM's [Watson Studio](http://dataplatform.ibm.com/). 

Click on New Project and select per below.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/create_prj.png)

Define the project by giving a Name and hit 'Create'.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/def_prj.png)

## 3. Add Data

[Clone this repo](https://github.com/IBM/predict-fraud-using-auto-ai)
Navigate to [data](https://github.com/IBM/predict-fraud-using-auto-ai/tree/master/data) and save the file on the disk. Review the data glossary from the data folder for more details. `Note: Citation is needed to use this dataset for any other projects.` 

Click on Assets and select Browse and add the csv file from your file system.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/add_asset.png)

# Steps using Jupyter Notebook

Follow the below steps to use Jupyter Notebook for building the model. This is to compare the manual process of model building with the automated process using AutoAI.

`Create an account with IBM Cloud and then create a project in Watson Studio. Add the data as an asset. These three steps are given above in detail.`

4. [Create the notebook](#4-create-the-notebook)
5. [Insert the data as dataframe](#5-insert-the-data-as-dataframe)
6. [Run the notebook](#6-run-the-notebook)
7. [Analyze the results](#7-analyze-the-results)


## 4. Create the notebook

* Open [IBM Watson Studio](https://dataplatform.ibm.com).
* Go to the project and click on Add 
* Click on `Create notebook` to create a notebook.
* Select the `From URL` tab.
* Enter a name for the notebook.
* Optionally, enter a description for the notebook.
* Enter this Notebook URL: https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/notebook/Fraud_Detect.ipynb
* Select the runtime (8 vCPU and 32GB RAM)
* Click the `Create` button.

After the notebook is imported, click on `Not Trusted` and select the option as Yes to trust the source of the notebook.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/not_trusted.png)

`This notebook has been created to demonstrate the steps for building the model using Watson Studio platform. For other usecases, the notebook has to be created from scratch.`

## 5. Insert the data as dataframe

Click on 0010 icon at the top right side which will bring up the data assets tab.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/add.png)

Click on Insert to code dropdown and select the option Insert Pandas Dataframe.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/insert_dataframe.png)

## 6. Run the notebook

When a notebook is executed, what is actually happening is that each code cell in
the notebook is executed, in order, from top to bottom.

Each code cell is selectable and is preceded by a tag in the left margin. The tag
format is `In [x]:`. Depending on the state of the notebook, the `x` can be:

* A blank, this indicates that the cell has never been executed.
* A number, this number represents the relative order this code step was executed.
* A `*`, this indicates that the cell is currently executing.

There are several ways to execute the code cells in your notebook:

* One cell at a time.
  * Select the cell, and then press the `Play` button in the toolbar.
* Batch mode, in sequential order.
  * From the `Cell` menu bar, there are several options available. For example, you
    can `Run All` cells in your notebook, or you can `Run All Below`, that will
    start executing from the first cell under the currently selected cell, and then
    continue executing all cells that follow.

## 7. Analyze the results

After we run the cells in the notebook which includes data ingestion, data analysis, splitting the data, building the model and generating feature importance, its time to review and analyze the performance. There could be so many other activities like handling missing values, outlier management, feature engineering and hyper parameters optimization which are omitted for demo purpose.

Check the model accuracy and confusion matrix to identify precision and recall scores. We can observe that model has > 92% accuracy on test data and the Precision/Recall scores are also high.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/cf_matrix.png)

Feature importance as per the model is below. The model has highlighted some of the attributes which has high impact on the outcome. Features might or might not be fairly compared to access the impact on outcome.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/feat_imp.png)

We have used shapley values which is a very effective model evaluation technique. Shapley values calculate the importance of a feature by comparing what a model predicts with and without the feature. However, since the order in which a model sees features can affect its predictions, this is done in every possible order, so that the features are fairly compared.

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/shap.png)

We can observe that attributes like Married, Applicant Income & Credit history available are having high impact on the outcome which is to detect fraud as per shapley values. 

![](https://github.com/IBM/predict-fraud-using-auto-ai/blob/master/images/shap_ft_imp.png)

With this, we have come to the end of this code pattern where we can compare the ease of using AutoAI to build predictive models vs creating a new jupyter notebook to build and evaluate predictive models. `There's considerable reduction of time in building and deploying the models using AutoAI because it handles missing values, outliers, feature engineering & hyper parameters optimization on the fly and selects the best algorithm as per the dataset.` AI Model building process has been reduced from Days to Hours thanks to `AutoAI.` If you are a developer or a data scientist who wants to build the model quickly and deploy it for being production ready, then AutoAI is for you which will help in taking decisions faster and gives a detailed overview of the attribute relationships within the data. 

## More to come :

The integration of Auto AI and Watson Open Scale is currently in progress and will be updated at a later date.

## Related Links :

[Fraud Prediction using skewed data](https://github.com/IBM/xgboost-smote-detect-fraud)

# Troubleshooting

[See DEBUGGING.md.](DEBUGGING.md)

## Citation for data :

`The dataset which is referenced in this code pattern is created and owned by R.K.Sharath Kumar, Data Scientist, IBM India Software Labs.`

# License

This code pattern is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the Developer [Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](http://www.apache.org/licenses/LICENSE-2.0.txt).

Check the [ASL FAQ link](http://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN) for more details

