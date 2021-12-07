

# Fairness Visualization Tools in ML Education

Here is a collection of sample demos and educational resources for Machine Learning Fairness Visualization tools, based on the paper 
> A Case Study of Integrating Fairness Visualization Tools in Machine Learning Education

## Aequitas

 Aequitas is a bias auditing toolkit developed by the Center for Data Science and Public Policy at the University of Chicago. Aequitas tools follow three steps: indicating which groups are analyzed and which are set as the reference group, analyzing bias based on desired metric (false negative, false discovery, etc) and a final pass/fail fairness indicator. Overall the tools are meant to generate reports that highlight disparities in predictive classification models. Aequitas offers visualizations of group parity, including graphics for parity tests and the magnitude of disparities between races, using a simple traffic light fail/pass visualization. 

Additionally, Aequitas offers tutorials for visualizing different disparities against user-designed attributes. The offered visualizations can be implemented through their online webapp, from a Python library, and as a command-line tool. The Aequitas Bias Report webapp uses two datasets for the purposes of their demo, the COMPAS Recidivism Risk Assessment dataset and the US Adult Income dataset, though users have the option to upload their own dataset. In order to use custom dataset, the dataset must adhere to a very strict format and contain a “score” column indicating the correctness of a prediction model and a “label_value” column indicating the actual value of the predicted label. In terms of the clarity of the tool and tutorial, the Aequitas website offers helpful descriptions of bias metrics and includes a fairness tree to help users decide which metrics to evaluate and decide their thresholds for fairness


**Resources:**

Github: https://github.com/dssg/aequitas

Web Application: http://aequitas.dssg.io/

Tool Guide: http://www.datasciencepublicpolicy.org/our-work/tools-guides/aequitas/

COMPAS Recidivism Risk Assessment Dataset: https://colab.research.google.com/github/dssg/aequitas/blob/update_compas_notebook/docs/source/examples/compas_demo.ipynb


## AI Fairness 360
As a comprehensive toolkit, IBM’s AI Fairness 360, or AIF360, contains multiple tools and algorithms to identify and mitigate bias and can be used for analysis of different metrics based on multiple use cases.  AIF360 also provides tools to measure fairness at different stages in the machine learning process. The 𝐷𝑎𝑡𝑎𝑠𝑒𝑡𝑀𝑒𝑡𝑟𝑖𝑐 class can be used to provide fairness metrics on the training data, while the 𝐶𝑙𝑎𝑠𝑠𝑖𝑓𝑖𝑐𝑎𝑡𝑖𝑜𝑛𝑀𝑒𝑡𝑟𝑖𝑐 class should be used to provide fairness metrics on the models themselves. In addition to fairness assessment it also offers pre-processing, in-processing and post-processing ways of mitigating biases. This toolkit is ideal for allocation and risk-assessment problems with defined protected attributes. AIF360 also is an open-source library with API documentation provided. There is support for this tool in the form of tutorial guides, videos, demos, and a notebook repository of working examples of the tool on the main site. This also provides resources for understanding applications of fairness and a glossary of introductory terms to fairness in ML.

**Resources**

GitHub: https://github.com/Trusted-AI/AIF360

Demo: http://aif360.mybluemix.net/data

Documentation: https://aif360.readthedocs.io/en/latest/



## Dalex
Dalex (moDel Agnositc Language for Exploration and eXplanation) is a an explainability tool created by ML2DataLab at Warsaw University of Technology and University of Warsaw. This project started in R and recently has been expanded to python. The Dalex Python package implements a main Explainer class to provide an abstract layer between distinct model API’s and the explainability and fairness methods.  Dalex comes with a full fairness tutorial on COMPAS recidivism and has a credit dataset based in Germany integrated within the package. Additionally, it provide tutorials for introductory explain-ability in AI to inform the appropriate methods available to explore a model.

**Resources:**
Website: https://dalex.drwhy.ai/

Github: https://github.com/ModelOriented/DALEX 

Tutorials: https://dalex.drwhy.ai/python/ 

Demo - COMPAS: https://dalex.drwhy.ai/python-dalex-fairness2.html

## Fairlearn
Fairless is a python tool developed by Microsoft to identify performance metrics on trained models. Fairlearn’s post-processing algorithms take an already-trained model and transform its predictions so that they satisfy the constraints implied by the selected fairness metric (e.g., demographic parity) while maximizing model performance (e.g., accuracy rate). 

For example, given a model that predicts the probability of defaulting on a loan, a post-processing algorithm will try to find a threshold above which an applicant should get a loan. Fairlearn’s reduction algorithms treat any standard classification or regression algorithm as a black box, and iteratively (a) re-weight the data points and (b) retrain the model after each re-weighting so that the model will satisfy the constraints implied by the selected fairness metric while maximizing model performance. Unlike the post-processing approach the reduction approach requires to re-train the model and so it could be slower. 

**Resources:**

Github: https://github.com/fairlearn/fairlearn

Documentation: https://fairlearn.org/main/quickstart.html

Demos (Download python notebooks): https://fairlearn.org/v0.7.0/auto_examples/index.html


## Responsibly
Responsibly is another fairness and auditing tool that is specifically developed for both researchers and learners with some features specialized for NLP analysis. It is compatible with data science and machine learning tools of trade in Python, such as Numpy, Pandas, and especially scikit-learn. 

Like the other tools we examined its first focus is on auditing biases and the secondary aim to enable mitigation. This contains fairness metrics for evaluating independence, separation, and sufficiency as well as analyzing various thresholds in post-processing methods. This tool is also closely linked with the terminology of used in the book of Fairness in Machine Learning by Barocas et al. that is used across various courses in ethics and fairness in multiple universities. It showcases fairness analysis using various datasets to demonstrate these features including visual plot capabilities and demonstrates Biases in Word Embedding with various datasets provided by Google, Facebook, and Stanford. Other available datasets include the Adult and the German Credit Dataset from UCI, the FICO Dataset from TransUnion, and COMPASS dataset by ProPublica.

**Resources:**

Github: https://github.com/ResponsiblyAI/responsibly

Documentation: https://docs.responsibly.ai/

Demo - COMPAS: https://docs.responsibly.ai/notebooks/demo-compas-analysis.html

Demo - Bias in Word Embedding: https://docs.responsibly.ai/notebooks/demo-word-embedding-bias.html

## What-if Tool
The What-If Tool from Google is built into the open source TensorBoard Web application and allows users to analyze a machine learning model performance and fairness. With the What-If Tool, users can test algorithmic fairness constraints, visualize inference results. One of the niche features of this tool is that it allows users to edit a datapoint to see how a model performs. This is useful for identifying counterfactual points in datasets. It also incorporates some inseparability into the model by allowing users to visualize partial dependency plots. What-If Tool offers other interactivity with performance of a classifier model (Confusion matrix) and ability to adjust threshold values in an intuitive GUI. As the tool is incorporated into TensorFlow, it provides the most visual experience of the toolkits listed here and enables easy integration of deep neural network models such as those for Face Recognition

**Resources:**

Website: https://pair-code.github.io/what-if-tool/

Github: https://github.com/pair-code/what-if-tool

Google Group: https://groups.google.com/g/what-if-tool 


Explanation - UCI Census: https://pair-code.github.io/what-if-tool/learn/tutorials/walkthrough/

Demo - UCI Census: https://colab.research.google.com/github/pair-code/what-if-tool/blob/master/WIT_Model_Comparison.ipynb
