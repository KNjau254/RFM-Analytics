# RFM-Analytics
In this Repo, I used Python to analyze the Recency, Frequency and Monetary value in order to gain insights into customer, understand their behavior and segment them.
Below are is step by step process I used in conductin the analysis:
Step I:
I imported the necessary libraries, such as pandas, plotly, and datetime, to perform the RFM analysis.

Step II:
I imported the RFM data from a CSV file into a pandas DataFrame. To ensure that the data was imported correctly, I displayed the first few rows of the DataFrame.

Step III:
To calculate the RFM values, I started by converting the 'PurchaseDate' column to a datetime format. Then, I calculated the recency of each customer by subtracting the purchase date from the current date. Additionally, I determined the frequency of purchases for each customer by counting the unique 'OrderID' values grouped by 'CustomerID'. Furthermore, I calculated the monetary value brought by each client by summing the 'TransactionAmount' values for each 'CustomerID'. I merged the frequency and monetary value data with the original RFM data.

Step IV:
I defined the scoring criteria for the recency, frequency, and monetary value. The scores were assigned based on the importance of each factor. For example, a higher score was assigned for more recent purchases, higher frequency, and greater monetary value.

Step V:
To perform further calculations, I converted the RFM scores to the numeric data type.

Step VI:
Using the defined scoring criteria, I calculated the final RFM score for each customer. The RFM score was obtained by summing the individual scores for recency, frequency, and monetary value.

Step VII:
To gain a better understanding of the RFM scores, I analyzed the descriptive statistics of the RFM scores, such as mean, standard deviation, minimum, maximum, and quartiles.

Step VIII:
To segment the customers based on their RFM scores, I divided them into three value segments: Low, Mid, and High. I assigned these segments using the qcut() function, which distributed the customers evenly among the segments.

Step IX:
To visualize the distribution of customers across the value segments, I calculated the count of customers in each segment. I then created a bar chart using plotly, which showed the number of customers in each value segment.

Step X:
Next, I analyzed the customer segments in broader classifications. I created a new column called 'RFM Customer Segment' and assigned the segments based on the RFM score ranges. For example, customers with an RFM score of 9 or higher were labeled as 'Loyalists'. I displayed the 'CustomerID' and 'RFM Customer Segment' columns to observe the segment assignment for each customer.

Step XI:
To analyze the distribution of RFM customer segments within each value segment, I calculated the count of customers in each RFM customer segment within each value segment. I then created a treemap chart using plotly, which visually represented the distribution of RFM customer segments within each value segment.

Step XII:
To gain further insights into the 'Loyalists' segment, I filtered the data to include only customers in this segment. I then created box plots using plotly to visualize the distribution of RFM values (recency, frequency, and monetary) within the 'Loyalists' segment.

Step XIII:
Similarly, I filtered the data to include only customers in the 'Potential Loyalists' segment. I created box plots using plotly to visualize the distribution of RFM values within this segment.

Step XIV:
To understand the correlation between the recency, frequency, and monetary scores within the 'Loyalists' segment, I calculated the correlation matrix. I visualized the correlation matrix using a heatmap, which helped me identify any relationships or patterns among the RFM values.

Step XV:
Similarly, I calculated the correlation matrix of the RFM values within the 'Potential Loyalists' segment and visualized it using a heatmap. This helped me understand the correlations between the RFM scores in this segment.

Step 15: I then highlighted the number of customers in each segment using a bar chart, demonstrating the distribution of customers across different RFM segments.

Step 16: Lastly I compared the average RFM scores for each segment using a grouped bar chart, providing a comprehensive view of the segments' characteristics.
