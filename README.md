# Crowdfunding_ETL

## Table of contents

* [Description](#Description)
* [Extract, Transform, Load](#Extract,-Transform,-Load)
* [Create the Contacts DataFrame](#Create-the-Contacts-DataFrame)
* [Create the Crowdfunding Database](#Create-the-Crowdfunding-Database)
* [ERD Image](#ERD-Image)
* [Questions](#Questions)
* [References](#References)

## Description

In this project we extract the data from the CSV data set, transforme and clean it to serve our purpuse, and load it into a database for storage so it can be used in future analysis.
The work in this project is divided into the following: 
- Create the Category and Subcategory DataFrames
- Create the Campaign DataFrame
- Create the Contacts DataFrame
- Create the Crowdfunding Database  

## Extract, Transform, Load

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns: 
* "category_id" column 
* "category" column 

2. Export the category DataFrame as category.csv
3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
* "subcategory_id" column 
* "subcategory" column 

4. Export the subcategory DataFrame as subcategory.csv

5. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

* The "cf_id" column
* The "contact_id" column
* The "company_name" column
* The "blurb" column, renamed to "description"
* The "goal" column, converted to the float data type
* The "pledged" column, converted to the float data type
* The "outcome" columnThe "backers_count" column
* The "country" column
* The "currency" column
* The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
* The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
* The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
* The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

## Create the Contacts DataFrame

Using Python dictionary methods we:

* Import the contacts.xlsx file into a DataFrame.
* Iterate through the DataFrame, converting each row to a dictionary.
* Iterate through each dictionary, doing the following:
- Extract the dictionary values from the keys by using a Python list comprehension.
- Add the values for each row to a new list.
* Create a new DataFrame that contains the extracted data.
* Split each "name" column value into a first and last name, and place each in a new column.
* Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

## Create the Crowdfunding Database

In this part we used QuickDBD to sketch an Entity Relationship Diagram (ERD) of the tables as follows:

* Use the information from the ERD to create a table schema for each CSV file and specifying the data types, primary keys, foreign keys, and other constraints.
* Create a new Postgres database, named crowdfunding_db.
* Using the database schema, create the tables in the correct order to handle the foreign keys.
* Verify the table creation by running a SELECT statement for each table.
* Import each CSV file into its corresponding SQL table.
* Verify that each table has the correct data by running a SELECT statement for each. The following image when running the SELECT statement: 

![Running the SELECT statement](/Resources/crowdfunding_db_schema.gif)

## ERD Image

![Entity Relationship Diagram](/Resources/crowdfunding_db_schema.png)

## Questions

In case of any additional questions please visit my GitHub link: [Feda2020](https://github.com/Feda2020) 

## References

* Stach Overflow (https://stackoverflow.com/)
* Xpert Learning (https://bootcampspot.com)