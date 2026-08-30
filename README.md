# Prediction with Regression Algorithms


## What is regression?

Regression analysis is a form of predictive modelling technique which investigates the relationship between a dependent (target) and independent variable (s) (predictor). In simple terms the regression can be defined as, "Using the relationship between variables to find the best fit line or the regression equation that can be used to make predictions."

This technique is commonly used for forecasting, time series modeling, and identifying causal relationships between variables. Several regression techniques are available to make predictions, and these techniques are primarily influenced by three factors: the number of independent variables, the type of dependent variable, and the shape of the regression line.

![Regression model](/images/Regression.png)
<p align="center">Figure 1: Regression Model</p>


## Project Description


This project implements and compares regression algorithms to predict housing prices based on features such as location, size, and property attributes. Using Python and scikit-learn, the project explores multiple models:

- Linear Regression
- Polynomial Regression
- Decision Trees
- Random Forests

These models are evaluated using metrics like Mean Squared Error (MSE) and R2 to assess performance and accuracy. Data preprocessing steps such as handling missing values, feature scaling, and splitting datasets ensure the models are trained and tested optimally.


## 1. Simple Linear Regression

The goal of a linear regression model is to establish a relationship between one or more independent variables (features) and a continuous dependent variable (target). When there is only one independent variable, it is referred to as Univariate Linear Regression, whereas the presence of multiple independent variables is known as Multiple Linear Regression.

<p align="center" style="font-size: 18px;"> General equation: y = w0 + w1 * x1</p>



## 2. Multiple Linear Regression

Multiple linear regression is used to estimate the relationship between two or more independent variables and one dependent variable. This statistical method models the dependent variable as a linear combination of the independent variables and is widely used to predict outcomes and analyze relationships in various domains.
<div align="center">

![multiple linear regression](/images/multi_linear_regression2.png)

</div>
<p align="center">Figure 2: Multiple Linear Regression Model</p>



## 3. Polynomial Regression

Polynomial Regression is an extension of Linear Regression that models the relationship between the dependent and independent variables as an n-degree polynomial. It is useful when the data exhibits a non-linear relationship that cannot be captured by a straight line.

Unlike simple linear regression, which assumes a linear relationship between the variables, polynomial regression fits a curvilinear equation.

![Polynomial_regression](/images/polynomial%20regression.png)
<p align="center">Figure 3: Polynomial Linear Regression Model</p>


## 4. Decision Tree Regression
A Decision Tree is a flowchart-like structure used in machine learning for both classification and regression tasks. Each node in the tree represents a decision or a test on a specific feature, directing the data to subsequent nodes based on the outcome of the test. The tree structure continues to split the data into smaller subsets until it reaches a terminal node, known as a leaf, which provides the final prediction as an output.

In a Decision Tree:

- Root Node: Represents the initial dataset and contains the first decision or test to split the data.
- Internal Nodes: Represent decisions or conditions based on one feature. Each internal node splits the data into two or more branches.
- Leaf Nodes: Represent the outcome or prediction (e.g., a class label for classification or a numeric value for regression).

![Decision_tree_img](/images/decision%20tree.png)
<p align="center">Figure 4: Decision Tree Regression Model</p>


## 5. Random Forest Regression
Random Forest is an ensemble learning algorithm used for classification and regression tasks. It operates by constructing multiple decision trees during training and combines their outputs (majority vote for classification or average for regression) to produce a more accurate and robust prediction. By aggregating the results of many decision trees, Random Forest reduces the risk of overfitting and increases the model's generalization ability.


![Random_Forrest_Regression](/images/random_forrest.png)
<p align="center">Figure 5: Random Forest Regression Model</p>


## Model evaluation
There are three main errors (metrics) used to evaluate regression models, Mean absolute error, Mean Squared error and R2 score.

**Mean Absolute Error (MAE)** The average magnitude of prediction errors in the same unit as the dependent variable.

- 0 indicates a perfect fit.

**Mean Squared Error (MSE)** is the average of the squared errors, so it penalizes large errors far more severely than MAE.

- A value of 0 indicates a perfect fit.

**R-squared (R2 )** tells us the degree to which the model explains the variance in the data. In other words how much better it is than just predicting the mean.

- 1: Perfect fit.
- 0: Model explains no variance.
- < 0: Model performs worse than simply predicting the mean


## Model results
### Comparative Performance
| Model                     | Mean Absolute Error (MAE) | Mean Squared Error (MSE) | R2 Score  |
|---------------------------|---------------------------|---------------------------|----------|
| Simple Linear Regression  | 0.26                      | 0.12                      | 0.37     |
| Multiple Linear Regression| 0.14                      | 0.04                      | 0.80     |
| Polynomial Regression     | 0.26                      | 0.12                      | 0.38     |
| Decision Tree Regression  | 0.16                      | 0.05                      | 0.74     |
| Random Forest Regression  | 0.13                      | 0.03                      | 0.82     |

Every figure above is the printed output of the matching notebook in `models/`, measured on the 20 percent test split with `random_state=42` under scikit-learn 1.9.0.

### **Observations**
The regression model comparison above shows that Random Forest Regression stands out with an R2 Score of 0.82, thereby offering the highest predictive accuracy. Multiple Linear Regression also performs well, reinforcing that model's adept at handling various predictors and complex interactions excel with this type of data. In contrast, Simple Linear Regression and Polynomial Regression struggle with lower R2 scores around 0.37, underscoring their limitations for complex datasets. Decision Tree Regression strikes a practical balance, combining effectiveness with model clarity. 

## Quick Start Guide

This guide provides instructions to quickly set up and run regression models in either Google Colab or your local environment. Each script is fully compatible with Google Colab notebooks.

### Using Google Colab

In Google Colab, most necessary packages like `pandas`, `numpy`, `scikit-learn`, and `matplotlib` are pre-installed. If additional packages are required, they can be installed directly at the top of your Colab notebook using:

```bash
!pip install package_name
```
### Running Locally

To run the scripts on your local machine, ensure you have Python installed. Follow these steps to prepare your environment:

#### 1. Clone the Repository
Clone the repository to your local machine using the following command:
```bash
git clone https://github.com/danielcoblentz/housing-price-regression
```
#### 2. Activate the virtual environment
You will need to activate the virtual environment.

```
Windows: .venv\Scripts\Activate
Mac: source .venv/bin/activate
```


### Execution
After activating the environment, open the notebooks and run them top to bottom:
```
jupyter notebook models/
```
## References

[Stanford Stats 202 course materials](https://web.stanford.edu/class/stats202/notes/Linear-regression/Simple-linear-regression.html)  
[ResearchGate Random Forest Example](https://www.researchgate.net/publication/350297716/figure/fig5/AS:11431281115895819@1675137747948/An-example-of-a-random-forest-structure-considering-multiple-decision-trees.png)  
[Decision Tree - GeeksforGeeks](https://www.geeksforgeeks.org/decision-tree/)  
[Scikit-learn](https://scikit-learn.org/stable/)  
[Scikit-learn Decision Trees Example](https://scikit-learn.org/1.5/auto_examples/tree/plot_tree_regression.html)  
[Keras Guide](https://keras.io/guides/)  
[Multiple Linear Regression - Scribbr](https://www.scribbr.com/statistics/multiple-linear-regression/)  
[Machine Learning - IBM](https://www.ibm.com/topics/machine-learning)  

