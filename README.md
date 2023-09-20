# NoSQL Challenge
### Contributor: "Alice" Lan Nguyen

### Overview
This project uses the database establishments.json, which includes information about various establishments across the United Kingdom. The primary objective is to analyze food hygiene rating data to help journalists and food critics in determining where to focus their future articles.

### Setting Up and Cleaning the Database (NoSQL_setup_starter.ipynb)
In this Jupyter Notebook, the following tasks were performed to prepare and cleanse the database for subsequent analysis:
- Data Import: The JSON file was imported directly from the Terminal to initialize the database.
- Adding Data: A document about a new halal restaurant was added to the existing database, and the corresponding business type ID was updated.
- Data Filtering: As establishments in Dover are not needed, I filtered and removed any establishments within Dover Local Authority from the database.
- Data Cleaning: I converted the numbers in the database to their correct data types.

### Analyzing the Database (NoSQL_analysis_starter.ipynb)
In this Jupyter Notebook, the prepared database from the previous step was used for in-depth analysis. The following analyses were conducted:
- I used query to identify establishments with a hygiene score equal to 20.
- I used $regex operator to find establishments in London, and used comparison operator to find places that have rating greater than 4.
- I used comparison operators to compare geocode to find establishments nearest to the newly added restaurant, then results were sorted by lowest hygiene score. Finally I used limit operator to find the top 5 establishments.
- I builded a data pipeline to find establishments in each Local Authority area with a hygiene score of 0. Then I sorted the results from highest to lowest and printed out the top 10 local authority areas.

All the results are converted into Pandas DataFrame for future utilization.