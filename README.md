# Predicting the Resources of Network Simulations

This is the repository for the 'Predicting the Resources of Network Simulations' project. This project is developed as a Student Master Project by the department of sustainable communication networks, University of Bremen, Germany.

 - [comnets.uni-bremen.de](https://www.uni-bremen.de/comnets)
 - [ComNets @Twitter](https://twitter.com/ComNetsBremen)
 - [ComNets @Youtube](https://www.youtube.com/c/ComNetsBremen)

## Abstract
The OOTB platform uses containerization techniques to run several simulations in parallel where each simulation takes certain amount of available resources and time to complete. It is important to demarcate or halt simulations that take longer durations and more resources to complete than 
usual as they hinder performing parallel simulations.

This project provides a solution to overcome this problem by training a Machine learning model and using it to predict the resources prior to the simulation and give an estimate to the user about the network resource utilization.

## Methodology

**Install**

This project requires **Python** and the following Python libraries installed:
-   [NumPy](http://www.numpy.org/)
-   [Pandas](http://pandas.pydata.org/)
-   [matplotlib](http://matplotlib.org/)
-   [scikit-learn](http://scikit-learn.org/stable/)
- [JSON](https://pypi.org/project/jsons/)
- [pickle](https://pypi.org/project/pickle5/)
- [yellowbrick](https://www.scikit-yb.org/en/latest/quickstart.html)
- [Regular Expression](https://docs.python.org/3/library/re.html)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://jupyter.org/install.html).
If you do not have Python installed yet, it is highly recommended that you run and execute on [Google Colab](https://colab.research.google.com/), which already has the above packages and more included.

**Data**

The data used for building the model in this project is obtained by performing simulations on OOTB tool. Once the required number of simulations are performed the user can also get these simulation results from the ‘Collect Simulation Data’ tab in the OOTB in JSON format. And the required data related to the simulation parameters can be extracted using the [JSONExtraction.ipynb](https://colab.research.google.com/github/Srikanth635/COMNETS/blob/main/Source_Code/JSONExtraction.ipynb)

The dataset used for the training the models in this project is available in the root/[Dataset](https://github.com/Srikanth635/COMNETS/tree/main/Dataset) folder

**Features**

 -  Number of Nodes
 - Data Generation Interval
 - Data Size in bytes
 - Constraint Area X
 - Constraint Area Y
 - Locations
 - Hosts
 - Maximum Cache Size
 - Forwarding Layer
 - Application Layer
 
 **Targets**
 - Peak Disk Usage
 - Peak RAM Used in Simulation
 - Peak RAM Used in Results parsing
 - Total Job Time Taken
 
**Models**

 **[Random Forest Regression](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)**
 Random Forest is an ensemble learning technique that involves creation of several individual 
decision trees in parallel and averaging the results of each tree which eventually results in a more powerful predictive model. 

**[eXtreme Gradient Boost Regression](https://xgboost.readthedocs.io/en/stable/index.html)**
Extreme Gradient Boosting (XGBoost) is an open source library with an efficient and scalable 
implementation of the gradient boosting framework. It is an ensemble boosting technique that involves building multiple individual base learners sequentially and combines them to obtain more accurate and powerful predictive model.

**Run**
Both the models can be executed through the colab links provided in the respective models in the root/[Source_Code](https://github.com/Srikanth635/COMNETS/tree/main/Source_Code)  folder.

All the evaluation graphs and results are available in root/[Results/Evaluation Graphs](https://github.com/Srikanth635/COMNETS/tree/main/Results/Evalaution%20Graphs) folder
