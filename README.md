# nosql-challenge

# UK Food Hygiene Rating Analysis

## Introduction

This project was commissioned by the editors of the food magazine, Eat Safe, Love, to evaluate the food hygiene ratings of various establishments across the United Kingdom. The goal is to assist journalists and food critics in deciding where to focus future articles based on the analysis of food hygiene ratings data.

## Part 1: Database and Jupyter Notebook Set Up

### Getting Started

- Using the `NoSQL_setup_starter.ipynb` notebook for the initial setup.
- Importing the `establishments.json` file into MongoDB. Use the Terminal for this operation and name the database `uk_food` and the collection `establishments`. Record the command used in a markdown cell within the notebook.


### Database Confirmation

1. Creating an instance of the Mongo Client.
2. Listing all databases to confirm the existence of `uk_food`.
3. Listing all collections in `uk_food` to ensure `establishments` is present.
4. Using `find_one` and `pprint` to display a single document from the `establishments` collection.
5. Assigning the `establishments` collection to a variable for easier access.

## Part 2: Update the Database

### Modifications Required

- Continue using the `NoSQL_setup_starter.ipynb` notebook.
- Adding a new halal restaurant in Greenwich to the database with specific details provided.
- Finding the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update the new restaurant entry with this ID.
- Removing all establishments located within the Dover Local Authority.
- Converting latitude, longitude, and `RatingValue` fields from strings to appropriate numeric types using `update_many`.

## Part 3: Exploratory Analysis

### Analysis Objectives

- Switch to `NoSQL_analysis_starter.ipynb` for this part.
- Understand that `RatingValue` ranges from 1-5, with higher values indicating better ratings. Non-numeric values such as 'Pass' will be treated as nulls.
- Scores for Hygiene, Structural, and ConfidenceInManagement are inversely related to establishment quality.

### Analysis Questions

Explore the database to answer the following:

1. Identifying which establishments have a hygiene score equal to 20?
2. Identifying establishments in London with a `RatingValue` ≥ 4.
3. Finding the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score and proximity to "Penang Flavours".
4. Determining how many establishments in each Local Authority area have a hygiene score of 0, sorting the results from highest to lowest and displaying the top ten.

### Deliverables

- Using `count_documents` for counts, `pprint` for displaying documents, and convert results to Pandas DataFrames for detailed analysis.
- Providing insights for each question, including document counts, DataFrame row counts, and the first 10 rows for detailed questions.

