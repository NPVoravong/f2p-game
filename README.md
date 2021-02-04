# Pandas Challenge

## Prompt
Using the provided dataset for the fictional free-to-play video game generate a report that includes the following items:  
1. Total Number of Players  
2. Purchasing Analysis (Total)  
    * Number of Unique Items
    * Average Purchase Price
    * Total Number of Purchases
    * Total Revenue
3. Gender Demographics
    * Percentage and Count of Male Players
    * Percentage and Count of Female Players
    * Percentage and Count of Other / Non-Disclosed  
4. Purchasing Analysis (Gender)  
    * Purchase Count
    * Average Purchase Price
    * Total Purchase Value
    * Average Purchase Total per Person by Gender  
5. Age Demographics  
_The below each broken into bins of 4 years (i.e. <10, 10-14, 15-19, etc.)_
    * Purchase Count
    * Average Purchase Price
    * Total Purchase Value
    * Average Purchase Total per Person by Age Group
6. Top Spenders  
_Identify the the top 5 spenders in the game by total purchase value, then list (in a table):_
    * SN
    * Purchase Count
    * Average Purchase Price
    * Total Purchase Value  
7. Most Popular Items  
_Identify the 5 most popular items by purchase count, then list (in a table):_  
    * Item ID
    * Item Name
    * Purchase Count
    * Item Price
    * Total Purchase Value  
8. Most Profitable Items  
_Identify the 5 most profitable items by total purchase value, then list (in a table):_
    * Item ID
    * Item Name
    * Purchase Count
    * Item Price
    * Total Purchase Value
  
## Process  
- **Dependencies and Setup**  
    * Pandas
    * Numpy  
    
  The data is stored in a CSV to read the csv we use Panda's `read_csv()` and save it to a variable. A master dataframe in created from that CSV. Now we can use the dataset throughout the jupyter notebook.  
  
  <img src="/images/final-map.png" height="auto"> Dataframe

1. **Total Number of Players** 
  Each row within the CSV is different purchase within the game. However, there is no limit on how many purchases a player can make so using the total number of purchases won't work. To find the actual number of players we need to get the number of unique player names and count the length of that list. `value_counts()` can be used on the dataframe to confirm that some players made more than one purchase.

<img src="/images/final-map.png" height="auto"> ValueCount

2. **Purchasing Analysis (Total)**  
To get the purchasing data we're interested the full dataframe needs to be trimmed down to just the relevant data. This reduced data is then converted into a dictionary with the data points of interst as the keys and the formulas to get the numbers as the values. The raw numberical values are fomatted using `.map()` and the appropritate format tag to make the data more readable.

<img src="/images/final-map.png" height="auto"> Purchase

3. **Gender Demographics** 
Gender is the CSV is divided into three categories female, non-disclosed, and male. The get a dataframe for each with just the relevant gender `.loc()` is used on the master dataframe. These three new dataframes are then used to create a final dataframe that shows all the statistics of interest on one table. Gender is set as the index for readability.  

4. **Purchasing Analysis (Gender)** 







  
  
   

