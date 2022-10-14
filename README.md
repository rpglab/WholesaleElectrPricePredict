## Wholesale Electricity Price Forecasting using Integrated Long-term Recurrent Convolutional Network Model
This is a set of python codes that forecast electricity price in wholesale power markets using an integrated long-term recurrent convolutional network (Integrated LRCN) model: day-ahead price prediction and hour-ahead price prediction. LRCN is a combination of LSTM and CNN.


### Data files:
*dataset_train_4_0to200.csv* 

1. Temperature data for the Houston region – Weather API. Using a python code, collected the temperature data using API call from the server of the website.

2. ERCOT price data: From ercot website, taking real time wholesale electricity price for a specific zone i.e. Houston area for four entire years: 2015-2018. Temporal resolution is an hour. 

3. ERCOT load data: From ercot website, historical load data for each weather zone in the ercot region is got. Houston comes in the coast zone.


### Model files:
 1. "SVM.ipynb" file: Support vector regression (SVR) model is set as benchmark based on the historic data to subsequently predict the wholesale electricity price.
		   
 2. "Linear_reg": The multilayer perceptron (MTP) is a fully connected neural network (FCNN) architecture with one input layer, multiple hidden layers, and one output layer. All the neurons of the previous layer are fully connected to the neurons of the next layer.
		   
3. "LRCN_Prediction" file:
   - Normalize the raw Dataset using Min-Max and One Hot Encoding methods.
   - Build Long-term Recurrent Convolutional Network Model.
   - Conditional error correction term that is added to the price forecasted by the LRCN model to establish the price prediction.  
         
4. "LSTM_Prediction" file        
   - Normalize the raw Dataset using Min-Max and One Hot Encoding methods.
   - Build LSTM Network Model.

Note:
With different input variables - there are two types of price forecasting: day-ahead and hour-ahead.


## Citation:
If you use these codes for your work, please cite the following paper:

Vasudharini Sridharan, Mingjian Tuo and Xingpeng Li, "Wholesale Electricity Price Forecasting using Integrated Long-term Recurrent Convolutional Network Model",https://arxiv.org/abs/2112.13681.

Paper website: https://rpglab.github.io/papers/Vasu-MJTuo_Price-Prdctn-ILRCN/


## Contributions:
This program was initially created by Vasudharini Sridharan, and then modified and cleaned up by Mingjian Tuo. Xingpeng Li supervised this work.


## Contact:
If you need any techinical support, please feel free to reach out to Vasudharini Sridharan at vasusridharan50@gmail.com or Mingjian Tuo at mtuo@uh.edu.

For collaboration, please contact Dr. Xingpeng Li at xli83@central.uh.edu.

Website: <a class="off" href="/"  target="_blank">https://rpglab.github.io/</a>


## License:
This work is licensed under the terms of the <a class="off" href="https://creativecommons.org/licenses/by/4.0/"  target="_blank">Creative Commons Attribution 4.0 (CC BY 4.0) license.</a>


## Disclaimer:
The authors don’t make any warranty for the accuracy, completeness, or usefulness of any information disclosed; and the author assumes no liability or responsibility for any errors or omissions for the information (data/code/results etc) disclosed.

