
# Marketing Analytics

Entally, an online retail business, is facing significant challenges with reduced customer engagement and conversion rates despite launching several new marketing campaigns. This project aims to conduct a detailed analysis to identify the underlying issues and areas for improvement in their marketing strategies. By understanding the factors contributing to the decline in customer interactions and conversions, as well as analyzing customer feedback, we can provide actionable insights and recommendations to enhance their marketing effectiveness, optimize expenses, and ultimately improve business outcomes

## Problem Statement

[Marketing Analytics.pptx](https://github.com/user-attachments/files/18614098/Marketing.Analytics.pptx)

![Image](https://github.com/user-attachments/assets/6f3516e6-dd50-45c3-aa89-051714ce4e6f)

![Image](https://github.com/user-attachments/assets/11de1c2a-80ca-4582-8718-23f1cad9a165)

![Image](https://github.com/user-attachments/assets/7160486e-82a9-41cc-b140-529f0a4a1e04)

![Image](https://github.com/user-attachments/assets/048a525f-8029-41ad-9e90-781708c43ccd)

![Image](https://github.com/user-attachments/assets/446abb5f-177e-40e5-8461-9dcaf9259eec)


## Analysis

For this project, we have the tables in MS SQL Server, we will be modifying the tables in MS SQL Server itself before taking them to Power BI

First, we take the products table and remove the category as all the products are from the same category and add a price category column to categorize the products under Low, Medium and High price

![Image](https://github.com/user-attachments/assets/efb06a79-d9e3-4649-a819-ad48044fdef1)

Next, we join the customer table with the geography table so that we have the customer and their geography information and in a single table rather than two tables

![Image](https://github.com/user-attachments/assets/9b186c2e-6c10-4284-b54e-e9824fa4cb91)

After this, we come to the customer review table. This table looks good but we observe some of the customer review text has double spaces instead of single space. We will need to change everything to single space in order to standardize the text

![Image](https://github.com/user-attachments/assets/3d5ba2e0-0cf9-449c-83e6-d3da902e3f11)

Coming to the customer engagement data table, we see that there re quite a few changes required. For example, the engagement date is in a different format than what we want, so we will need to format that, View and Clicks are combined in a column so we will need to separate those out into two columns, Content type has some values in upper case, some in lower case and some with spaces and some without, so we will need to standardize those 

Lastly, we will be excluding out the Content type Newsletter as we are not taking that into consideration for our analysis 

![Image](https://github.com/user-attachments/assets/00f3cdcb-90db-47cd-a548-4afedafc8e82)

Coming to the last table customer journey, we see suspect that there might be duplicate data here, so we run the SQL command and find that yes that is correct

![Image](https://github.com/user-attachments/assets/7a7da2e1-c0d5-44b4-ab35-40a498e92250)

So we need to remove the duplicates and also there a few NULL values in the duration column, we decide to use the average duration to replace the NULL values

![Image](https://github.com/user-attachments/assets/4e659809-88eb-435c-ae27-169a960ff4d6)
