# project3-Semi-Structure-Data-Analytics-
Export data from MongoDB to json.file and import it into visual studio code, and then import jupyter notebook for data analysis.
This repository will tell you:
Use the data from MongoDB sample: sample_supplies
Find the following queries.

1.Show top 10 products (name) sales (quantity x price).

2.Show top 3 products (name) sales by store (location).

3.Show rankings of each store (location).

4.Show purchased method by gender table


<img width="139" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/dcad5344-9698-4dd9-b6ee-2f1d0d692f8c">

5.Show monthly total sales

The tool i will use VSCode Notebook

<img width="1278" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/2fe61133-23c9-436c-b180-f2386848b924">


First
We need to export database 'sample_supplies' from MongoDB
<img width="1279" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/e42016d2-77a1-436c-8687-ca8a3ed0860e">

So if we want to use jupyter notebook in visual studio code, we need to connect them first.
We click'connect' button, then choose MongoDB for VS Code

<img width="74" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/91c68a17-49e4-4e3b-bf04-1163f8f5cff9">

Then you can open this page

<img width="592" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/1efa950a-8d45-4451-b1b7-a8c21aee99b1">

Then you should copy this link

<img width="568" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/8d44b1d0-14c6-4b8d-b989-5e302e35d26c">

Second
we will go to the visual studio code, then connect the MongoDB
before you connect it, you need to download the extension of MongoDB

<img width="1273" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/fb9094ff-f20f-4a34-83b4-91ec3ea1ad2e">

Then you use the link that copy from MongoDB, you should paste this link to top search box of the visual studio code

<img width="1004" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/d839dbdd-0e57-4628-9cee-a4e6abe52553">

Then click 'connect' button to connect them

<img width="185" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/8a8864e8-7c0a-4c28-aed1-d8d1a35585a9">

I believe it will be successful!

Third
when you have connected them
you can see the all the databases from MongoDB, then you can use them to do what do you want

<img width="190" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/c927f87b-e26e-4e81-843f-a2f77e11f724">

our goal is export 'sample_supplies' to json file, then import this file to jupyter notebook in VSC(visual studio code)

So now we have a important step, and we need open our command prompt
before you use command prompt, you should make sure you download the mongo tool, then you can use mongo commands

<img width="867" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/89f00f64-88b8-4b85-bfe9-feb2711f879e">

if you download mongo tool successfully, when you input 'mongoexport' or 'mongoimport', you should can see it like the below figure

<img width="571" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/de3ada14-aac3-4aaf-a026-621751ecc943">

if we want to export "sample_supplies" out ,we need a command name"mongoexport"
there is a command you can use it

mongoexport --uri="mongodb+srv://6338324:HCZ123456@cluster0.79wampg.mongodb.net/sample_supplies" --collection="sales" --out=sales.json

<img width="849" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/eae3b47b-b126-4fff-b569-364aceec2b9e">

1. mongoexport: This is a command-line tool for MongoDB used to export data from a MongoDB database.

2. --uri="mongodb+srv://6338324:HCZ123456@cluster0.79wampg.mongodb.net/sample_supplies": This is the connection URI for MongoDB, which includes the connection details.you can get this link from vsc,you click your cluster
Then right click on it, and you'll see "Copy Connection String."

<img width="275" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/8efbabb6-6279-4ace-be37-6448de9fb38d">

   
3. --collection="sales": This specifies the name of the collection (table) from which data should be exported. In this case, data will be exported from a collection named "sales."

4. --out=sales.json: This specifies the name of the JSON file where the exported data will be saved. In this case, the data will be exported to a file named "sales.json."

When you check the directory, you can see the sales.json file

<img width="379" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/489f3aa3-0547-4aa9-a4ef-70efbf8e6c7a">

Fourth
Now we already have a sales.json file, so we can start to use it in the jupyter notebook of vsc
If you want to use jupyter notebook in vsc, remember you need to download the 'jupyter notebook'extension first

<img width="1057" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/b4d7425d-efc2-4e2c-9c0a-5cff453c9207">

now we can begin to program

First step

If we want to analyze the data, there are two necessary libraires we need, they are pandas and matplotlib 
Pandas: Pandas is an open-source data manipulation and analysis library for Python. It provides easy-to-use data structures and data analysis tools for working with structured data, such as tabular data, time series data, and more. 

<img width="165" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/8a7c6a20-b813-4ac7-beb1-37eb7333455d">

Matplotlib: Matplotlib is a popular Python library for creating static, animated, and interactive visualizations in a wide range of formats. It provides a comprehensive set of tools for constructing various types of plots, charts, and graphs.

<img width="188" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/e2333850-4834-47b1-9e7b-cdcfe985f1e9">

Second step

we need import the sales.json file in jupyter notebook

<img width="521" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/db9211f2-b5d7-4833-a576-505f2c848edd">

Third step

Now we start to solve the queries（I will analyze it from three aspects:Preparation, Processing ,Result  ）

1.Show top 10 products (name) sales (quantity x price).

<img width="661" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/ab5ab71f-4c7f-4843-bcf9-bac8c6478c82">

Explanation:

Preparation:
The code starts by importing the necessary libraries, including Pandas and JSON.
It opens a JSON file, reads it line by line, and parses each line as a JSON object. These objects are then stored in a Python list.

Processing:
It creates a Pandas DataFrame, converting the list of JSON objects prepared earlier into a DataFrame.
Using the explode method, it unpacks the 'items' column of the DataFrame into separate rows because the 'items' column contains multiple product entries that need to be split for sales calculations.
It calculates the total sales for each product, which is the product's quantity multiplied by its price.
It groups the data by product name using the groupby method, sums the total sales, and finds the top 10 products by sales.
It uses the nlargest(10) method to find the top 10 products with the highest sales, as required by the problem.

Results:
Several column renaming operations are performed to ensure that the column names match the description in the problem statement.
Finally, by calling top_10_products, the code displays a list of the top 10 products with the highest sales, including product names and sales figures.

2.Show top 3 products (name) sales by store (location).

<img width="987" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/54b81715-16de-4a47-bb77-d79df8bc3816">

Explanation:

Preparation:
It directly operates on the DataFrame data.

Processing:
The code begins by grouping the data by both the product name ('name') and the store location ('storeLocation'). It sums the total sales for each unique combination of product and store location.
It then uses the nlargest(3) method to find the top 3 products by sales for each store location. This operation is carried out independently for each store location, ensuring that the top products are calculated per store.
Column renaming operations are performed to ensure that the column names match the problem description.

Results:
The final result is displayed, showing the top 3 products (by name) and their respective sales for each store location. Each row in the result represents a product, its sales, and the store location where these sales occurred.

3.Show rankings of each store (location).

<img width="520" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/7d07dc67-44e5-466d-b238-71c2de70e82e">

Explanation:

Preparation:
It directly operates on the DataFrame data.

Processing:
The code starts by grouping the data by the 'storeLocation' column, effectively creating groups for each unique store location.
It sums the total sales for each store location using the sum() function, creating a new DataFrame named store_rankings that includes the store locations and their respective total sales.
It then ranks the stores based on total sales using the rank method. The rank method assigns a rank to each store's total sales in descending order (high sales receive a lower rank) and uses the 'min' method to handle ties by giving each tied value the lowest possible rank.
The stores are sorted by their rank in ascending order using the sort_values method, so that the highest-ranking store is listed first.

Results:
The final result is displayed as the 'store_rankings' DataFrame, which shows the rankings of each store location based on their total sales. Each row in the result represents a store location, its total sales, and its rank.

4.Show purchased method by gender table

<img width="629" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/26ed340c-af80-472a-95f9-6d6ad3a6d704">

Explanation:

Preparation:
It directly operates on the DataFrame data.
It extracts the 'gender' information from the 'customer' column and creates a new 'gender' column in the DataFrame. It checks if the 'gender' key exists in each 'customer' dictionary, and if it does, it extracts the gender information; otherwise, it assigns None.
It excludes rows with the 'purchaseMethod' value equal to 'Phone', effectively filtering out purchases made by phone.

Processing:
The code uses the pd.crosstab function to pivot the data and create a table that shows the count of purchase methods by gender. This function is used to cross-tabulate the 'gender' and 'purchaseMethod' columns.
It renames the columns for better clarity, mapping 'Online' to 'Online' and 'In store' to 'In-Store'.
It renames the index to 'Female' and 'Male' for better clarity.
The code removes the title for the columns to have a cleaner representation of the data.

Results:
The final result is displayed as the 'purchase_method_gender_table,' which is a table that shows the count of purchase methods by gender, with 'Female' and 'Male' as the index and 'Online' and 'In-Store' as the columns.

5.Show monthly total sales

<img width="605" alt="image" src="https://github.com/CHENZHENHE/project3-Semi-Structure-Data-Analytics-/assets/118869086/e33baf5b-1318-4dd7-9c79-188c144e75b5">

Explanation:

Preparation:
The code begins by loading JSON data into a Pandas DataFrame. The JSON data is assumed to be stored in a file located at the given file path.
A custom date parsing function, custom_date_parser, is defined to extract date information from the 'saleDate' column. This function handles dates provided in a specific format that includes the '$date' key.
The custom date parser is applied to the 'saleDate' column, converting the date strings into Pandas datetime objects.

Processing:
A function, calculate_sales, is defined to calculate sales for each row. It iterates through the 'items' within each row and computes the sales for each item by multiplying the quantity with the item price.
The calculate_sales function is applied to each row using the apply method with axis=1. This results in the calculation of sales for each sale transaction.
New columns 'Year' and 'Month' are created by extracting the year and month from the 'saleDate' column. This allows grouping the data by year and month.
The code then groups the data by 'Year' and 'Month' and calculates the sum of 'sales' for each group using the groupby method.

Results:
The final result is a Series named 'monthly_sales' that shows the total sales for each month and year. It is displayed as the output.


That's all we've done. I hope this article has been helpful to you. If you have any questions, feel free to ask me and we can talk more about it.

Thanks 
