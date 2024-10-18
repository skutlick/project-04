# Predicting Marathon Finish Times Using Neural Networks

### Abstract
>This project investigates the use of neural networks to predict marathon finish times, aiming to enhance our understanding of performance metrics in long-distance running. By analyzing historical marathon data and applying various data preprocessing techniques, we explore the relationship between various factors and finishing times. We employed Keras Tuner for hyperparameter optimization and experimented with different network architectures to identify the most effective model. While our efforts yielded an accuracy of X%, the results revealed challenges in reliably predicting finish times. Despite these limitations, the insights gained from our approach provide a foundation for future research and applications in sports analytics.

### Introduction
>Marathons are a significant athletic challenge, traditionally measuring 26.2 miles (42.195 kilometers). The distance was standardized in 1908 during the London Marathon when the starting line was moved to accommodate the royal family. This project aims to explore whether we can accurately predict the finish time of a marathon winner using neural networks.

### Fun Facts About Marathons
>Current marathon records:
- Men's Record: 2:00:35 by Kelvin Kiptum of Kenya at the Chicago Marathon.
- Women's Record: 2:09:56 by Ruth Chepngetich of Kenya at the Chicago Marathon.</br>
Approximately one million people complete a marathon each year.
<img title="Raw Marathon Winner Data" alt="Alt text" src="/output_data/prjt_4_raw_data_scatter.png">

### Project Objective
>The main objective of this project is to determine if we can accurately predict the finish time of a marathon winner using neural networks.

### Process
>Data Preprocessing (ETL Breakdown)
- Dependencies: Installed Keras Tuner for model optimization and imported necessary libraries.
- Data Import: Read in the CSV data containing marathon finish times and runner information.
- Data Type Conversion: Converted marathon finish times from object to seconds using pd.to_datetime().
- Categorical Variables: Transformed categorical variables into indicator variables using pd.get_dummies().
- Data Splitting: Separated the data into target and feature variables and utilized train_test_split() to create training and testing sets.

### Choosing a Neural Network
>Data Visualization: Graphed the training data to understand its structure, which informed the choice of activation function.
Data Complexity Analysis: Analyzed the complexity and sparsity of the data to determine the appropriate mathematical computations.
Network Experimentation: Experimented with different activation functions and network densities to optimize performance.
<img title="indicator variables standarized" alt="Alt text" src="/output_data/X_train_graph_1.png">

### Optimizing the Neural Network
>Feature Engineering: Created a new column for 'decade' from the 'year' column and converted it into an indicator variable using get_dummies().
Hyperparameter Tuning: Utilized Keras Tuner for auto-optimization to identify the best model configuration.
<img title="data withh all indicator variables standarized" alt="Alt text" src="/output_data/X_train_graph_2.png">

### Results
>Based on our calculations and comparison graphs, our model achieved an accuracy approximate to 1.0 on average in predicting marathon finish times. Visualizations of our results can be seen on the graph below.</br> That line is the percentage of predictions over actual finish times. 
<img title="model predictions over actual time" alt="Alt text" src="/output_data/nn_model_over_actual.png">

### Observations
>The auto-optimization using Keras Tuner for hyperparameters did not yield a model that could reliably predict finish times.</br> However, the insights gained from data preprocessing and model optimization will guide future efforts in this area.
<img title="Berlin Marathon Predictions vs. Actual" alt="Alt text" src="/output_data/berlin_act_vs_pred_cleaned.png">

>The Boston Marathon had the most available data, going back to 1897.  In the graph below, we can see a significant spike in both the actual winning marathon times, as well as in our linear regression predicted times.  This is explained by the introductoin of female runners within the dataset, as the Boston Marathon allowed women to compete in 1966.</br> 
<img title="Boston Marathon Predictions vs. Actual" alt="Alt text" src="/output_data/boston_all.png">

>Separating out the Boston Marathon data across genders presents a tighter linear regression model fit when looking at just Male runners.  Additionally, we can observe a clear decline in overall winning race times over the past 120+ years</br> 
<img title="Boston Marathon Predictions vs. Actual - Male Runners" alt="Alt text" src="/output_data/boston_male.png">

>Looking at just female runners of the Boston Marathon we can see a similar decline of winning times in both the actual data, as well as the predicted data, however it is not as pronounced as observed in the male-only dataset.  Additionally, the linear regression model did not fit that well or accurately within that first decade (1967 to 1977) of introducing female runners within the dataset.</br> 
<img title="Boston Marathon Predictions vs. Actual - Female Runners" alt="Alt text" src="/output_data/boston_female.png">


### Conclusion
>This project demonstrates the potential of using neural networks for predictive analysis in sports. </br> While our initial attempts did not produce a usable model, the insights and methodologies developed during this project will inform future research and applications in the field.

##### Citations
[Fun Fact Data](https://www.ineos159challenge.com/news/the-history-of-the-marathon) </br>
[Code Correction through Google Colab](https://colab.research.google.com/) </br>
[Code Correction with Xpert Learning](https://bootcampspot.instructure.com/courses/5580/external_tools/313) </br>
[Assistant for checking language](https://chatgpt.com)
