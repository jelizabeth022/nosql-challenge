# NoSQL Challenge

![image](https://github.com/user-attachments/assets/1949d2a0-957e-4360-8617-ba3019e9b2e2)

# Overview
This repository contains the code and resources for the NoSQL Challenge. The UK Food Standards Agency evaluates various establishments across the United Kingdom and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data to help their journalists and food critics decide where to focus future articles.

# Table of Contents

Overview

- Instructions

- Part 1: Database and Jupyter Notebook Set Up

- Part 2: Update the Database

- Part 3: Exploratory Analysis

- Setup

- Usage

- Contributing

- License

# Instructions

# Part 1: Database and Jupyter Notebook Set Up

1. Import the Data:

- Import the data provided in the establishments.json file from your Terminal.

- Name the database uk_food and the collection establishments.

- Copy the text you used to import your data from your Terminal to a markdown cell in 
  your notebook.

2. Set Up the Jupyter Notebook:

- Import the libraries you need: PyMongo and Pretty Print (pprint).

- Create an instance of the Mongo Client.

- Confirm that you created the database and loaded the data properly by:

  - Listing the databases you have in MongoDB and ensuring that uk_food is listed.

  - Listing the collection(s) in the database to ensure that establishments is there.

  - Finding and displaying one document in the establishments collection using find_one     and displaying with pprint.

  - Assigning the establishments collection to a variable to prepare the collection for     use.
 
# Part 2: Update the Database

1. Insert New Data:

Insert the following information for a new halal restaurant into the database:

2. Update Data:

- Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the 
  BusinessTypeID and BusinessType fields.

- Update the new restaurant with the BusinessTypeID you found.

3. Remove Specific Data:

- Check how many documents contain the Dover Local Authority.

- Remove any establishments within the Dover Local Authority from the database.

- Check the number of documents to ensure they were deleted.

4. Update Data Types:

- Use update_many to convert latitude and longitude to decimal numbers.

- Use update_many to convert RatingValue to integer numbers.

# Part 3: Exploratory Analysis

1. Find Establishments with Hygiene Score Equal to 20:

- Perform a query to find the establishments with a hygiene score of 20.

- Use count_documents() to list the number of documents.

- Print the first result using pprint.

- Convert the results to a Pandas DataFrame and display the first 10 rows.

2. Find Establishments in London with RatingValue Greater Than or Equal to 4:

- Perform a query to find the establishments in London with a RatingValue greater than 
  or equal to 4.

- Use $regex to locate the London establishments.

- Use count_documents() to list the number of documents.

- Print the first result using pprint.

- Convert the results to a Pandas DataFrame and display the first 10 rows.

2. Find Top 5 Establishments with RatingValue of 5, Nearest to "Penang Flavours":

- Perform a query to find the establishments within 0.01 degree of the "Penang 
  Flavours" restaurant.

- Limit the results to establishments with a RatingValue of 5.

- Sort by the lowest hygiene score.

- Limit the results to 5.

- Print all five results using pprint.

- Convert the results to a Pandas DataFrame and display them.

4. Find Top Local Authorities with Hygiene Score of 0:

- Build an aggregation pipeline to include a match query, group, and sort.

- Match documents with a hygiene score of 0.

- Group on LocalAuthorityName and count the number of documents.

- Sort the count in descending order.

- Send the aggregation pipeline to the aggregate() method.

- Print the first ten results using pprint.

- Convert the results to a Pandas DataFrame and display the first 10 rows.

# Usage

To run the MongoDB shell and follow the CRUD operations for gardenDB, use the MongoDB shell commands as outlined in the instructions.

# Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes or additions.

# License
This project is licensed under the MIT License. See the LICENSE file for details.
