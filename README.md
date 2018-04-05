# General Assembly Challenge

## Explanation
### Summary

- Statistics:
1. Smaller mean radius than those diagnosed as 'malign'
2. Smaller median radius than those diagnosed as 'malign'
3. Smaller standard deviation than those diagnosed as 'malign'
4. The group diagnosed as B also has smoother histogram

- Approach:
The approach taken in this analysis is by using the logistic regression model to fit the data given with the dependent variable as the diagnosis and the independent variables are attributes of other measurements such as mean radius of a tumor.

With such approach, we were able to determine, with 94% accuracy, whether a tumor is malignant or not.

- Why logistic regression?
Logistic regression is a simple to understand model that works well with binary variables, namely 1 or 0. Logistic regression's outcome is either 1 or 0 depending on the threshold for cut off. For example if the expression returns the value of 0.7, and if our cutoff value is 0.5, we categorize it as 1 (and if <0.5 we can categorize as 0).

Illustration of logistic regression:
https://upload.wikimedia.org/wikipedia/commons/6/6d/Exam_pass_logistic_curve.jpeg

### Limitation of such approach

One of the limitations of using such model is that we assume the variables are all independent. However, it can be argued that at least some of the variables are not independent with one another. For example, we assumed that mean radius and the texture mean of a tumor are independent. But could it be that they would both be larger or smaller together?

In addition, we could be potentially overfitting the model. In this analysis we used 30 features to predict the outcome of the diagnosis without backwards or forward pruning of the features. Such can lead to overfitting and may actually give us worse outcome than if we were to include fewer variables.

## Appendix
### Step by Step Setup to Run Code

1. Install Jupyter Notebook, Pandas
```
pip3 install jupyter
pip3 install pandas
pip3 install scipy
pip3 install sklearn
pip3 install statsmodels
```
2. Launch Jupyter Notebook
```
jupyter notebook
```
3. Run all cells
