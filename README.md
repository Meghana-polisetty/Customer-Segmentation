# Customer-Segmentation
RFM (Recency, Frequency, Monetary) model to determine which segments of customers should be targeted to enhance revenue for automobile bike company, by grouping customers into 11 segments based on previous purchase transactions.

# Data Analytics Customer Segmentation

## Goal of the project

The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing a RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions. In this analysis the customer segment was divided into 11 groups. The analysis will help in determining which customers segments should be targeted in order to enhance sales revenue for the company. A Sales Dashboard for Customer Segmentation is developed using Tableau and the data quality assessment and analysis is done using Python.

## Datasets Used

* The datasets used include:
    * Raw_data.xlsx: This excel file dataset included the following sheets of data:
    * Transactions_data.xlsx: This dataset included the transactions data of the customers across all the different states in Australia.
    * NewCustomerList.xlsx: This dataset included the new customers who visted the automobile bike company recently.
    * CustomerDemographic.xlsx: This dataset included entire details of the Customer Demographics.
    * CustomerAddress.xlsx: This dataset included the address of the Customers.
 
## Tools and Technologies used

The tools used in this project include:

* Python - This was needed to conduct Data Quality Assessment and also for Data Cleaning processes. With Python libraries pandas, matplotlib, seaborn exploratory data analysis of the datasets and to gain useful insights from the data was possible.

* Tableau - This Business Intelligence tool was required to explore data and create charts, graphs, visualizations to come up with a Sales Dashboard for Customer Segmenatation for the automobile bike company.

## Tableau Dashboard

The Sales Dashboard for Customer Segmentation

![image](https://user-images.githubusercontent.com/90289879/198737530-63430bf9-c738-4f73-bccb-901550e47fa3.png)

## Analysis Approach

1. Data Quality Assessment and Data Cleaning

The first step towards generating useful insights from the data was the data prepartion, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

In the data cleaning step the data quality of the following datasets were first assesed. After a data quality assessment the following data quality issues was observed and the necessary process to mitigate the issue was followed :

* CustomerDemographics.xlsx :
   * 1 Irrelevent column was present and such columns were dropped from the dataset.
   * There were 5 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped        or appropiate values were imputed at places of missing values
   * For gender column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
   * The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution. An            outlier was observed and the record was removed.
   * Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.
* NewCustomerList.xlsx :
   * 5 Irrelevent column was present and such columns were dropped from the dataset.
   * There were 4 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped        or appropiate values were imputed at places of missing values
   * The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution.
   * There was no data inconsistency.
   * Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

* Transaction_data.xlsx :
  * The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.
  * There were 7 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped       or appropiate values were imputed at places of missing values
  * A new feature column 'Profit' was created which is basically the difference between list price and standard price.
  * There was no data inconsistency.
  * Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.
* CustomerAddress.xlsx :
  * For states column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
  * There were certain customer IDs from Customer Dempgraphics table which were getting dropped in the Address table.
  
2. Exploratory Data Analysis on Customer Segments

After the data cleaning process, exploratory analysis on the dataset is performed and the following insights are obtained :

* New vs Old Customers Age Distribution
  * Most New customers are aged between 40-49 also for Old Customers the most of them are aged between 40-49
  * The lowest number of customers for both the types of customers is present in the age bracket under 20 and above 80 age groups.
  * The automobile company is popular among New Customers among the age groups 20-29 and 40-49.
  * A steep drop in customers is observed in the 30-39 age group among the New Customers
![image](https://user-images.githubusercontent.com/90289879/198738720-543876ce-e5ab-4e0e-b920-1e9361bfd0fa.png)

* Bike purchases over last 3 years by Gender
  * Most bike puechases are done by Feamale over the last 3 years. Approximately 51% of the bike purchases are done by Female compared to 49% of the         purchases being done by Male.
  * The Female purchases are 10,000 more than that of Male purchases (numerically).
![image](https://user-images.githubusercontent.com/90289879/198738773-06187e2a-2193-4e9b-a0d3-a61c9e206345.png)

* New vs Old Customers Job Industry Distribution
  * Most New customers are from the Manufacturing and Financial Services sector (approx 20% of the New Customers).
  * The lowest number of customers are from the Agriculture and Telecom sector approx 3%.
  * Similar trend is observed among Old Customers as well.
![image](https://user-images.githubusercontent.com/90289879/198738827-a85c68b1-aac0-49e6-a24b-4ca024f0bb7d.png)

* Wealth Segmentation by Age Category
  * Across all age categories the largest number of customers are from 'Mass Customer' Segment
  * The next category comes from the 'High Net Worth' customers.
  * In the age group 40-49, Affluent segment out performs the High Net Worth customers in terms of number of customers.
![image](https://user-images.githubusercontent.com/90289879/198738889-f9133478-86b3-4b05-97f2-1532f8df3d2d.png)

* Cars owned by States
  * New South Wales has the largest number of people who donot own a car.
  * In Victoria the proportion is quite even.
  * In Queensland the number of people owning a car is greater than who donot have a car.
![image](https://user-images.githubusercontent.com/90289879/198739007-32976946-e861-4a6b-8fcf-ae45f75092d7.png)

3. RFM Analysis and Customer Segmentation
In this stage of analysis the customer segmentation was done by developing an RFM Model. The RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions.

In this analysis the customer segment was divided into 11 groups. The groups being :

* Platinum Customers
* Very Loyal Customers
* Recent Customers
* Potential Customers
* Lost Customers
* Losing Customers
* Late Bloomer
* High Risk Customers
* Evasive Customers
* Becoming Loyal
* Almost lost Customers
* As of the current state of the Automobile business the current distribution of customers segments is depicted below:

![image](https://user-images.githubusercontent.com/90289879/198739087-1f49d298-ca57-44c1-ad10-a03aee9885bd.png)

4. RFM Analysis: Scatter Plots
Recency vs Monetary :
The visualization shows that recent customers have purchased more products and generated relatively more revenue than the customers who visited a while ageo.

![image](https://user-images.githubusercontent.com/90289879/198739100-dfd711c4-f5fe-40b9-a3e2-731dc2d698c6.png)

Frequency vs Monetary :
The visualization shows that customers belonging to Platinum/ Very Loyal/ Becoming Loyal Customer Segments have a greater frequency and generate greater monetary for the business
![image](https://user-images.githubusercontent.com/90289879/198739120-e503b19c-4506-4995-acd9-fcd3d8e31554.png)
