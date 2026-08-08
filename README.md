# Iran-Transactions-Analysis
* In this Data Analysis session I chose a dirty dataset from Kaggle that was based on Iran Transactions, I cleaned the data inside the Excel file and then used Power BI to visualize the results.
* The original dataset was downloaded from https://www.kaggle.com/datasets/hosseinbadrnezhad/dirty-iranian-transactions-dataset
* I have also provided both the original dataset and the one I have modified.


# Data preparation & Data Analysis
To start with, as soon as I downloaded the dataset, it needed some processing before the columns and their data became visible.
* I selected the **first column** -> **Data** -> **Text to Columns** -> **Delimited by comma**
* **CTRL A** -> **ALT** -> Type **HOI**
* **Bold the column headers.**

Then it was time for the Data Cleaning. This dataset was not something really hard to deal with. It includes 6 rows. Status, Date, Time, Card_type, City and Amount. At first, I noticed that in the column named “status,” which contains titles such as ‘success’ and “fail,” some began with a capital letter and some did not. So I created a new column named “status_new” that contains the same labels but with all letters capitalized to make it easier to filter them. Then, in the same column, in some rows, “success” was written as “succeed” and “fail” as “failed.” I replaced those. Finally, I deleted any remaining “nan” entries.
