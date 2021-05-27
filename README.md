# PREDICTING THE SALE PRICE OF BULLDOZERS USING MACHINE LEARNING

![bulldozer](https://user-images.githubusercontent.com/66157611/119805748-27498680-beff-11eb-8a4e-d56dbbfa8fac.jpg)


The data is taken from **Kaggle** competition : https://www.kaggle.com/c/bluebook-for-bulldozers/data

# PROBLEM DEFINATION

> How well can we predict the future sale price of a bulldozer,given its characteristics and previous examples of how much similar bulldozers have been sold for?

# OVERVIEW

## Prizes🏆

There are a $10,000 prize💰 pool for this competition, with prizes awarded to the top 3 places:

* 1st place:$6,500  
* 2nd place:$2,500
* 3rd place:$1000

## Description

The goal🎯 of the contest is to predict the sale price of a particular piece of heavy equiment at auction based on it's usage, equipment type, and configuaration.  The data is sourced from auction result postings and includes information on usage and equipment configurations.

Fast Iron is creating a "blue book for bull dozers," for customers to value what their heavy equipment fleet is worth at auction.

## Evaluation


_The Evaluation Metric_ for this competition is the **RMSLE (root mean squared log error)** between the actual and predicted auction prices.

## Data



![data](https://user-images.githubusercontent.com/66157611/119812502-d6895c00-bf05-11eb-9034-ffed864027ab.png)


**There are 3 main datasets**

**Train.csv** is the _training set_, which contains data through the end of 2011.

**Valid.csv** is the _validation set_, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.

**Test.csv** is the _test set_, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012. Your score on the test set determines your final rank for the competition.

## Features


| **Variable**                                           | **Description**|
|--------------------------------------------------------|----------------|
| SaleID |   Unique identifier of a particular sale of a machine at auction|
|MachineID	|  Identifier for a particular machine;  machines may have multiple sales|
|ModelID	|  Identifier for a unique machine model (i.e. fiModelDesc)|
|datasource|	  Source of the sale record;  some sources are more diligent about reporting attributes of the machine than others.  Note that a particular datasource may report on multiple auctioneerIDs.|
|auctioneerID|	  Identifier of a particular auctioneer, i.e. company that sold the machine at auction.  Not the same as datasource.|
|YearMade	 | Year of manufacturer of the Machine|
|MachineHoursCurrentMeter	 | Current usage of the machine in hours at time of sale (saledate);  null or 0 means no hours have been reported for that sale|
|UsageBand	|  Value (low, medium, high) calculated comparing this particular Machine-Sale hours to average usage for the fiBaseModel;  e.g. 'Low' means this machine has less hours given it's lifespan relative to average of fiBaseModel.|
|Saledate	|  Time of sale|
|Saleprice	|  Cost of sale in USD|
|fiModelDesc|	  Description of a unique machine model (see ModelID); concatenation of fiBaseModel & fiSecondaryDesc & fiModelSeries & fiModelDescriptor|
|fiBaseModel	 | Disaggregation of fiModelDesc|
|fiSecondaryDesc	|  Disaggregation of fiModelDesc|
|fiModelSeries	 | Disaggregation of fiModelDesc|
|fiModelDescriptor	|  Disaggregation of fiModelDesc|
|ProductSize	|  The size class grouping for a product group. Subsets within product group.|
|ProductClassDesc	|  Description of 2nd level hierarchical grouping (below ProductGroup) of fiModelDesc|
|State	|  US State in which sale occurred|
|ProductGroup	 | Identifier for top-level hierarchical grouping of fiModelDesc|
|ProductGroupDesc	 | Description of top-level hierarchical grouping of fiModelDesc|
|Drive_System	|machine configuration;  typcially describes whether 2 or 4 wheel drive|
|Enclosure	|machine configuration - does machine have an enclosed cab or not|
|Forks	|machine configuration - attachment used for lifting|
|Pad_Type|	machine configuration - type of treads a crawler machine uses|
|Ride_Control|	machine configuration - optional feature on loaders to make the ride smoother|
|Stick	|machine configuration - type of control |
|Transmission	|machine configuration - describes type of transmission;  typically automatic or manual|
|Turbocharged	|machine configuration - engine naturally aspirated or turbocharged|
|Blade_Extension|	machine configuration - extension of standard blade|
|Blade_Width	|machine configuration - width of blade|
|Enclosure_Type	|machine configuration - does machine have an enclosed cab or not|
|Engine_Horsepower	|machine configuration - engine horsepower rating|
|Hydraulics	|machine configuration - type of hydraulics|
|Pushblock	|machine configuration - option|
|Ripper	|machine configuration - implement attached to machine to till soil|
|Scarifier	|machine configuration - implement attached to machine to condition soil|
|Tip_control	|machine configuration - type of blade control|
|Tire_Size|	machine configuration - size of primary tires|
|Coupler	|machine configuration - type of implement interface|
|Coupler_System|	machine configuration - type of implement interface|
|Grouser_Tracks	|machine configuration - describes ground contact interface|
|Hydraulics_Flow|	machine configuration - normal or high flow hydraulic system|
|Track_Type	|machine configuration - type of treads a crawler machine uses|
|Undercarriage_Pad_Width|	machine configuration - width of crawler treads|
|Stick_Length	|machine configuration - length of machine digging implement|
|Thumb	machine |configuration - attachment used for grabbing|
|Pattern_Changer|	machine configuration - can adjust the operator control configuration to suit the user|
|Grouser_Type|	machine configuration - type of treads a crawler machine uses|
|Backhoe_Mounting|	machine configuration - optional interface used to add a backhoe attachment|
|Blade_Type	|machine configuration - describes type of blade|
|Travel_Controls	|machine configuration - describes operator control configuration|
|Differential_Type	|machine configuration - differential type, typically locking or standard|
|Steering_Controls	|machine configuration - describes operator control configuration|
	


