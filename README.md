# Iran-Transactions-Analysis
* In this Data Analysis session I chose a dirty dataset from Kaggle that was based on Iranian Transactions that took place in September 2025. I cleaned the data inside the Excel file and then used Power BI to visualize the results.
* The original dataset was downloaded from https://www.kaggle.com/datasets/hosseinbadrnezhad/dirty-iranian-transactions-dataset
* I have also provided both the original dataset and the one I have modified.


# Data preparation & Data Analysis
To start with, as soon as I downloaded the dataset, it needed some processing before the columns and their data became visible.
* I selected the **first column** -> **Data** -> **Text to Columns** -> **Delimited by comma**
* **CTRL A** -> **ALT** -> Type **HOI**
* **Bold the column headers.**

Then it was time for the Data Cleaning. This dataset was not something really hard to deal with. It includes 6 rows. Status, Date, Time, Card_type, City and Amount. 

At first, I noticed that in the column named “status,” which contains titles such as ‘success’ and “fail,” some began with a capital letter and some did not. So I created a new column named “status_new” that contains the same labels but with all letters capitalized to make it easier to filter them. Then, in the same column, in some rows, “success” was written as “succeed” and “fail” as “failed.” I replaced those. Finally, I deleted any remaining “nan” entries.


Next, I went to the “date” column. Things get a little more complicated there. I couldn't easily filter it, since I wanted to keep both the date and the time. The easy part is that it consists only of the days of September 2025. I created a new column and copied the data from the previous one into it. I converted this new column to the “Time” format on the Home tab and the old column to "Short Date". That way, I separated the date from the time and kept both pieces of data intact. 


Moving on to the next columns (card_type, city), a series of replacements follows, as the data here was quite messy. Using the Filter in the Data Tab, you can easily identify all the different values contained in the column. So, for example, I replaced TEHRAN, tehr@n, ThRan, and other such instances with Tehran. In addition, I deleted the rows containing "nan" values that were left at the end. In the next column, I made the same changes. That is, data such as "vsa", "MastCard", "Master-Card", were changed to "Visa" and "Master Card", respectively. 


Finally, in the last two columns (amount, id), I deleted quite a bit of data because there were incorrect entries and outliers. So, in the amount column, I deleted some extreme values, such as 0, 99999999, -9999999999, because, as you can understand, such transactions are not possible. In the "id" column, I removed several duplicates, since IDs are unique and refer to only one transaction. In fact, I noticed that many incorrect transaction values are associated with duplicate IDs, so it’s best to first clean up the transaction values and then the IDs.


We are now at the point where the data has undergone the necessary preprocessing steps and is ready to be imported into any visualization program, which in this case is Power BI.

# Power BI Analysis
In Power BI, I created a small dashboard with three different charts.


* The first chart shows the types of cards used for transactions (x-axis) in relation to the number of transactions made (y-axis). At the same time, I added a legend listing all the cities and sorted them in ascending order by the number of cities. The difference in Tehran’s figures is clearly evident, both in terms of payment cards and the number of cities using them.  
