# Marathon Winner Prediction 

### Intro
- How long is a marathon?
	- Fun facts marathons were 26 miles until 1908 London Marathon when the Queen of England requested the starting line be moved for the royal children to see the start. 
[history of a marathon]('https://www.ineos159challenge.com/news/the-history-of-the-marathon')

- Current marathon records?
	- Men's: 2:00:35 by Kelvin Kiptum of Kenya; Chicago
	- Women's: 2:09:56 by Ruth Chepngetich of Kenya; Chicago

- How many people complete one per year?
	- about a million persons
   
Slide 1
Can we accurately predict the finish time of a marathon winner using neural networks.

Slide 2
We believe we can.

Slide 3
Yes! Calculation and graphs
Based on comparison graphs and calculated fields of the data we determined that we are X% accurate

Slide 4
plot.show()

Slide 5 
- How did we get here?
- Preprocess the data (ETL breakdown)
	- Install keras-tuner
	- import dependencies
	- read in csv
	- determine the data types
	- change the marathon finish time from object to seconds using pd.to_datetime()
	- converted categorical variables into indicator variables using pd.get_dummies()
	- seperated the data into target and features
	- split the data using train_test_split()
- Choosing a Neural Network
	- first we graphed the X_train data to determine what the data looks like, this will help in choosing an activation function.
	- looked at the complexity of the data and determined that it may require simpler mathematical computations
	- considered the sparsity of the data once plot
	- finally experimented with different activation functions and density.
- Optimizing the Neural Network
	- after initial results we looked at ways to make the model more efficient
	- set 'year' column into 'decade' and converted to indicator variable using get_dummies()
	- used tuner to auto optimization and determine what is the best model
- Choosing the correct
***add column to csv output for nn_model***

- Observations/Graphs
	- auto optimization using tuner for hyperparameters did not yield a model that could be used to predict the time
	- 
