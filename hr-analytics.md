# Exploratory Analysis for a HR Analytics company

Our project objective was further streamlined into developing a model as Proof-of-Concept that predicts employee Attrition, based on available data, as collected by the Employers.

The focus for this presentation is the Visualizations created in the process of exploring the data. The purpose of these visualizations were twofold:

1. _Exploratory_ Analysis for discovering insights from the data in order to build a reliable Machine learning model, and also
2. _Communicating key business insights_ to business stakeholders.

The technology used for the Exploratory Analysis is the Python Programming Language, in a Jupyter Notebook Environment. Within the Python ecosystem, various libraries and packages were used, and are listed below:

1. Numpy
2. Pandas
3. Matplotlib

I used Power BI reports and dashboard to communicate critical business insights to stakeholders.

## Understanding the Business Problem

The first thing I did regarding the project was to get an overview of the domain context of the project. This was necessary to understand the business problem we were undertaking. The problem revolved around finding out the reasons why employees would leave a company.
Another importance of this phase was for me to determine what the objective of the project is, assess the situation, and develop a project plan.

Having a viable solution to this problem would enable employers to identify employees who are likely to quit and take steps to address whatever issues are motivating such employees to leave. Success criteria for this project was set at presenting a Machine Learning code as proof of concept for this problem, as well as a dashboard showing interesting insights on the dataset.

It took me about 8 hours of research and study to get familiar with the business problem of employee attrition.

## Understanding and Preparing the Data for Analysis

The next phase of the project involved getting an intimate understanding of the data provided for the project. The Dataset was presented in a spreadsheet format (Microsoft Excel), and contained 39 columns and 4387 rows. This data contained employee records in a company for each month, starting from January 2019 to December 2020.

The employee records contain largely the same employee names repeated every month (until the employee quits, or new employees join the company in subsequent months). The dataset contained various features that describe the employee’s gender, age, Date of Birth, marital status, Citizenship Description, Race, State of residence and zip code, vacation costs and weeks, absenteeism, and other like features. The data type of each feature column was noted for further analysis.

The dataset was labeled to indicate whether the employee is still employed in the company or not. This label was valid for each month and would change from 0 to 1 on the month the employee quits the company.

The dataset had no peculiar quality issues, save some instances where we had to derive new features from existing ones (Feature Engineering).
At this phase, data was read into the Python Environment using the pandas package, which provided me the functionality of viewing a description and summary statistics of the dataset.

Below is a snapshot of the code used to load the data into Python.

![image]()

## Exploratory Data Analysis

The objectives of this phase of the project are as follows:

1. Identify the Fields that we will used in the model, some could be calculated fields such as age, number of promotions etc.
2. Provide a clear explanation of why the field was chosen.
3. Start the Python program that will create a new data set with the fields identified above for Active employees in the last month.

First off, I had to carry out some preliminary data cleaning, by removing a column in the dataset that was not useful for the analysis, right from the beginning. After that, I performed some Feature Engineering by converting the Employee Date of Birth values to Employee Age. The same transformation was done with the year the employees joined the company. Number of years spent in the company would provide more analytical value.

The very next challenge was to obtain an aggregate dataset that contains unique employee records. This is because the original dataset contained repeated records for the same employees, who stayed employed over a period of months. This is because these employee records were generated monthly and appended together in the first place.

The Aggregation process involved passing a function through the dataset that returns a value if there were some changes in certain dataset features. After aggregation, I then carried out an Analysis of the aggregated dataset to determine if any of the employees had a significant change in their salary, position level, employee engagement and satisfaction levels. Only a couple of employees had a salary increase, and one of these two employees also had a promotion in the two-year period.

Also, after aggregation, the dataset now contained 311 unique employee records. The next step in analysis involved splitting the dataset into two parts, one part consisting of employees that have quit the company voluntarily (those who were fired for cause were filtered out, because they are not useful for our analysis) and those who remain employed. Then afterwards I created simple plots for each categorical feature to determine whether each feature has a significant impact on the outcome of employees leaving or staying. The plots were created in Python using the Matplotlib and Seaborn packages.

![image]()

The figure above shows a comparison of the number of employees who have quit the company, compared to those who remained. The figure below shows Employee Attrition by Gender, which indicates that gender has not real impact on Attrition.

![image]()

Conversely, the plot figure below shows that the marital status feature has an impact on Attrition. We notice a higher proportion of married and divorced employees leaving, more than those who are single.

![image]()

The final inference of this Analysis Exercise was to remove the features that have no significant impact on the prediction.
For the continuous features, I plotted a correlation matrix(heatmap), to identify and eliminate features that are cross correlated.

![image]()

Using several features with high correlation may not always have a negative effect on the model but removing one of them helps make the learning algorithm faster and decreases the risk of harmful bias. In summary, the fewer features, the simpler the model.
I used a benchmark of 0.7 correlation (+ve and -ve) between features. Where I found those, I removed one and kept the other.

In summary, the following are a sample of the conclusions I reached, regarding what features to retain and what features to drop:

1. Retain Vacation Days taken and drop Vacation costs.
2. Retain Unexcused Absenteeism and drop Cost of Unexcused Absenteeism
3. Retain Training Hours, drop Training Cost
4. Retain Annual Salary, drop Compensation Cost

In summary the proposed list of Columns to move ahead with for the prediction are listed below:

`['Date ', 'Employee Age', 'Marital Status', 'Race', 'Zip', 'Position ID', 'Annual Salary', 'Benefits (Monthly) ', 'Years in Company', 'Perf Score ID', 'Engagement Survey', 'Emp Satisfaction', 'Vacation Days Taken', 'Training hours ','Term Ind']`

Finally, from the modified dataset, I created a Train dataset that contains current employees and terminated employees before December 2020, and the number of employees in December 2020 as the Test Set. This is in preparation for the Machine Learning Phase.

## Visualization in Power BI

This phase involved creating a visual report that shows some insight into various features within the dataset.
Some key insights, inferred from the data include:

1. The various reasons given by employees for terminations that the employer needs to pay attention to. This is also evidenced by the Attrition, Compensation and Age visual.
2. Also, there seems to be a higher proportion of married and divorced employees leaving the company.
3. A large proportion of attrition is coming from employees in the Production Department.

![image]()

## Machine Learning Modeling and Evaluation - Bonus

At the beginning of this Phase, I loaded the Train and Test Datasets which were outputs from the Exploratory Data Analysis Phase. The Train dataset contained 307 records, whilst the Test set contained 208 records.

The Python packages used in this phase includes Scikit-learn, Tensorflow and Keras, in addition to Numpy, Pandas and Matplotlib.
After that, I proceeded to carry out Feature Encoding, which involved converting the categorical data types to a numerical form, so they can be understood by the Algorithm. I used the LabelEncoder method for the conversion.

Next up, I created the Train data and Label, as well as the test data and scaled the data using StandardScaler to standardize the data. Standardization (or z-score Normalization) is the procedure where the feature values are rescaled so that they have the properties of a standard normal distribution. In practice, this usually leads to an increased speed in the machine learning process.

Next, I created a 1-dimensional CNN (Convoluted Neural Network) model, which is a kind of Neural Network, using the Tensorflow and Keras Packages. This neural network has three hidden layers in between the input layer and the output layer. As per Machine Learning best practice, the activation function used was the ReLu function.

![image]()

The Neural Network Training was done in 20 epochs, until the training curve flattened, and the model reached an optimal validation accuracy value of 0.84. The model, when used to predict test cases, yielded a loss of 0.0667 and accuracy of 0.995.
However, due to the nature of this Analysis, there are some observations made that are limiting to the accuracy of the model.
The first challenge is that I have not yet found any example where CNN is used on tabular data. All the examples I saw during my research (including the example on the Tensorflow documentation) are done on image classification. So, a limitation exists in fitting a Convolutional layer on the data, outside of the 1D model.

Another challenge, I think, lies on not having enough data samples. I am having to split 307 sample train data records into training and validation sets, and I think it may not be enough to train a viable model.
I was using quite similar data, both for train and testing, although the data was partitioned at the last month. This is because, it is still largely the same employees involved, whose details did not change much (if at all) between November and December 2020.
My Recommendation is to stick with tried and tested Machine Learning methods in predicting Employee Attrition. A simple Logistic Regression, or any traditional Classification algorithm can be effective. Otherwise, a Multi-Layer Perceptron will be useful in creating this model.

![image]()
