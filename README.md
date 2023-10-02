# Bulldozer-SellPrice-Prediction

This project originated from a Kaggle competition ten years ago with the goal of predicting the sale prices of bulldozers based on historical bulldozer sale prices from previous years.
![image](https://github.com/this1shung/Bulldozer-SellPrice-Prediction/assets/126255184/03761807-10f3-4bda-92df-0c5cfd5f1bfe)

I will summarize information about this project below:
# Problem definition
 - This time, we will be predicting the sale price of bulldozers, which is a value that can go up or down. Therefore, this project will revolve around a regression problem, where we aim to predict a continuous numerical value (the sale price) based on various features and historical data.
# Data
 - The data for this project is provided by Kaggle : https://www.kaggle.com/competitions/bluebook-for-bulldozers/data
 - The dataset is divided into three parts:

   + Train.csv is the training set, which contains data through the end of 2011.
      
   + Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.
       
   + Test.csv is the test set, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012. Your score on the test set determines your final rank for the competition.
 - In addition to being a regression problem, this project primarily focuses on the data preprocessing aspect i have performed several data preprocessing steps(across the train,valid and test data) to create a suitable dataset:

   + When initially working with the dataset, I observed that the date values are stored as an 'object' data type instead of the 'datetime' data type. Therefore, I had to change it.
       
   + A significant portion of the data was also missing
       
   + I also encountered a significant amount of non-numeric data (data that needed to be transformed for machine learning models to understand). During this process, I converted object data types into numerical types, and I also handled missing data.
# Features
 - There are many attributes in the dataset, and I will list 10 of them here. In the notebook , I also performed a step to find feature importance to determine which attributes have the most significant impact on the model's predictions. Here are 10 attributes from the dataset:

   1.SalesID: Unique identifier of a particular sale of a machine at auction

   2.MachineID: Identifier for a particular machine; machines may have multiple sales

   3.ModelID: Identifier for a unique machine model (i.e. fiModelDesc)

   4.Datasource: Source of the sale record; some sources are more diligent about reporting attributes of the machine than others. Note that a particular datasource may report on multiple auctioneerIDs.

   5.auctioneerID: Identifier of a particular auctioneer, i.e. company that sold the machine at auction. Not the same as datasource.

   6.YearMade: Year of manufacturer of the Machine

   7.MachineHoursCurrentMeter: Current usage of the machine in hours at time of sale (saledate); null or 0 means no hours have been reported for that sale

   8.UsageBand: Value (low, medium, high) calculated comparing this particular Machine-Sale hours to average usage for the fiBaseModel; e.g. 'Low' means this machine has less hours given it's lifespan 
   relative to average of fiBaseModel.

   9.Saledate: Time of sale

   10.Saleprice: Cost of sale in USD(only appear in train set and valid set)
# Evaluation metrics
 - The evaluation metric specified by Kaggle for the project is Root Mean Squared Log Error (RMSLE). In addition to that, i have also used the R-squared (R2) metric and some other evaluation metric.
# Model 
 - After trying various regression model, I didn't find any other model as effective as the RandomForestRegressor. Therefore, I decided to focus on using and improving it.
# Wrapping Up 
 - Above is the summary of the project I have provided, and all the code and workflow are documented in the notebook.
 - Here is some picture of my work:
  ![image](https://github.com/this1shung/Bulldozer-SellPrice-Prediction/assets/126255184/358f3900-3165-491b-9d0e-41ad6b872eba)
  ![image](https://github.com/this1shung/Bulldozer-SellPrice-Prediction/assets/126255184/450f8a59-dbdb-4105-a136-3a3f60cf5ffd)
  ![image](https://github.com/this1shung/Bulldozer-SellPrice-Prediction/assets/126255184/f75def63-b62f-49e9-af6b-9b40a6bf64bd)
  ![image](https://github.com/this1shung/Bulldozer-SellPrice-Prediction/assets/126255184/8d5cb423-3210-4704-87f1-00d9e69b5d89)

Thank you for reading my project details, and if you come across any issues or errors in my project, please do inform me. It will be helpful for me. Wishing you a great day!

## 📫 How to reach me: <a href="https://hungmondaypkm@gmail.com" target="blank"><img align="center" src="https://img.icons8.com/color/48/000000/gmail--v2.png" alt="hungmondaypkm@gmail.com" height="30" width="40" /></a><a href="https://www.facebook.com/profile.php?id=100009216758210" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="1" height="30" width="40" /></a><a href="https://twitter.com/gnuhmonday" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="1" height="30" width="40" /></a><a href="https://www.linkedin.com/in/quang-h%C6%B0ng-l%C3%AA-989610293/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="1" height="30" width="40" /></a>

