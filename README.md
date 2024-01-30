
# Retail Store


## Problem Statement

1. The CEO of the retail store is interested to view the time series of the revenue data for the year 2011 only. He would like to view granular data by looking into revenue for each month. The CEO is interested in viewing the seasonal trends and wants to dig deeper into why these trends occur. This analysis will be helpful for the CEO to forecast for the next year.

2. The CMO is interested in viewing the top 10 countries which are generating the highest revenue. Additionally, the CMO is also interested in viewing the quantity sold along with the revenue generated. The CMO does not want to have the United Kingdom in this visual.

3. The CMO of the online retail store wants to view the information on the top 10 customers by revenue. He is interested in a visual that shows the greatest revenue generating customer at the start and gradually declines to the lower revenue generating customers. The CMO wants to target the higher revenue generating customers and ensure that they remain satisfied with their products.

4. The CEO is looking to gain insights on the demand for their products. He wants to look at all countries and see which regions have the greatest demand for their products. Once the CEO gets an idea of the regions that have high demand, he will initiate an expansion strategy which will allow the company to target these areas and generate more business from these regions. He wants to view the entire data on a single view without the need to scroll or hover over the data points to identify the demand. There is no need to show data for the United Kingdom as the CEO is more interested in viewing the countries that have expansion opportunities.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open the table view and check all the columns. 
- Step 3 : During data cleaning process, remove negative values from "Quantity" column because quantity should not be below than 1 unit and remove negavite values from "UnitPrice" column because Unit price should not be below $0.
- Step 4 : For calculating revenue, creating new column following DAX expression was written;
Revenue = 
        
        'Online Retail'[Quantity]*'Online Retail'[UnitPrice]
        
- Step 5 : In the report view, under the view tab, theme was selected. 
- Step 6 : Question 1: Visual filters were added for two fields named "InvoiceDate" & "Revenue". 
        using visual level filter from the filter pane, Advanced filtering was used for year selection from InvoiceDate and line chart was selected from visualizations.
        
        Snap of Revenue by Month

![2024-01-30](https://github.com/Muskan145/Retail_Store/assets/105537965/db60dd76-3f9e-4f2d-b8fc-4e325308ee67)


- Step 7 : Question 2: Visual filters were added for three fields named "Country", "Quantity" & "Revenue"
        using visual level filter from the filter pane, Advanced filtering was used for "Country" to select top 10 countries by revenue and UK was excluded.
        
        Snap of Quantity and Revenue by Country

![2024-01-30 (1)](https://github.com/Muskan145/Retail_Store/assets/105537965/477b58f3-5496-4ef7-8ffa-6dfff957db6d)


- Step 8 : Question 3: Visual filters were added for two fields named "CustomerID" & "Revenue". 
        using visual level filter from the filter pane, Advanced filtering was used for "CustomerID" to select top 10 customers by revenue and (Blank)CustomerID was excluded.
        
        Snap of Revenue by CustomerID

![2024-01-30 (2)](https://github.com/Muskan145/Retail_Store/assets/105537965/d37c777e-987f-4645-955d-267d682a13ac)


- Step 9 : Question 4: Visual filters were added for two fields named "Country" & "Quantity". 
           UK was excluded and style was change "Grayscale" from map setting in visualizations
         
         Snap of Quantity by Country

![2024-01-30 (3)](https://github.com/Muskan145/Retail_Store/assets/105537965/0c96a0e3-0745-4703-931d-8a141c490c69)
  
# Insights

Following inferences can be drawn from the Questions;

### [1] There are some months of the year where exceptional growth is witnessed.

   Revenue in the first 8 months is fairly constant as the average revenue generated for these 8 months is around $685k.

   The increase in revenue starts in the month of September, where the revenue increases by 40% over the perivious months.

   This trend continues till the month of November where it reached 1.5 million USD, the highest during the entire year.

           This analysis shows that the retail store sales are impacted by the seasonality which usually occurs in the last 4 months of the year.
           
### [2] The countries where demand can be increased

Netherlands (194K units), Ireland (141K units), Germany (112K units) and France (107K units) have high volumes
of units bought and revenue generated.


        I would suggest that these countries should be focused on to ensure that measures are taken to capture these markets even more.  
  
  ### [3] Top 10 customers who have purchased the most from the store.
There is not much of a difference between the purchases
made by the top 10 customers. 

The highest revenue generating customer only purchased 17%
more than the 2nd highest


        This shows that the bargaining power of customers is low and the business is in a good position.

 ### [4] regions that have generated the most revenue
 
 Countries such as Netherlands, Ireland, Germany, France and Australia are generating high revenue and the company should
invest more in these areas to increase demand for products. 

The map also shows that most of the sales are only in the European region with very few in the American region. Africa and Asia do not have any demand for the products, along with Russia.

        A new strategy targeting these areas has the potential to boost sales revenues and profitability. # Retail_Store
