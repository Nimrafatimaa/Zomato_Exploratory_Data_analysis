 # Zomato Exploratory Data Analysis Project

## Project Overview

An exploratory data analysis project on a Zomato restaurant dataset in Python examining restaurant categories, customer votes, ratings, online ordering, table booking, and approximate cost for two people. Pandas is used to prepare and summarize the data, while Matplotlib and Seaborn visualize patterns across the dataset.

## Objectives

- Inspect the dataset structure and summary statistics.
- Prepare the rating and column names for analysis.
- Check missing values and duplicate records.
- Compare restaurant types by votes, count, average rating, and estimated cost.
- Explore ratings against votes and online-ordering availability.

## Tools

Python, Jupyter Notebook, Pandas, NumPy, Matplotlib, and Seaborn.

## Dataset

The supplied CSV (`zomato_data(1).csv`) contains 148 rows and 7 columns examined at the restaurant-record level:

- **Restaurant Name:** Restaurant name
- **Online_Order:** Online order availability
- **Book_Table:** Table booking availability
- **Rate:** Rating in x/5 format
- **Votes:** Number of customer votes
- **Approx_Cost(For Two People):** Approximate cost for two (renamed to `approx_cost`)
- **Listed_In(Type):** Restaurant category

## Data Cleaning

- Converted text ratings (such as `4.1/5`) to numeric float values using `handleRate`.
- Standardized column names to lowercase and renamed `approx_cost(for two people)` to `approx_cost`.
- Confirmed 0 missing values and 0 duplicate rows across all 148 records.

## Exploratory Data Analysis & Questions

The analysis uses grouped summaries, a pivot table, and visualizations (pie chart, horizontal bar chart, scatter plot, count plot, histogram, boxplot, and heatmap) to answer ten questions:

1. How many customer votes has each restaurant type received?
2. How many restaurants offer table booking?
3. Which five restaurants have the highest number of votes?
4. Is there a relationship between restaurant ratings and customer votes?
5. What is the average rating for each restaurant type?
6. Which restaurant type is most common in the dataset?
7. What ratings do restaurants most commonly receive?
8. Which restaurant type has the highest average cost for two people?
9. Do restaurants offering online ordering have higher ratings?
10. Which restaurant types have more records without online ordering?

## Key Findings

- **Votes by type:** Dining received the most votes (20,363), followed by other (9,367), Cafes (6,434), and Buffet (3,028).
- **Table booking:** Available in 8 records (5.4%) and unavailable in 140 records (94.6%).
- **Top 5 by votes:** Empire Restaurant leads with 4,884 votes, followed by Meghana Foods (4,401), Onesta appearing twice (2,556 votes each), and Kabab Magic (1,720).
- **Ratings vs. votes:** Moderate positive correlation ($r \approx 0.49$) between ratings and customer votes.
- **Average rating by type:** Highest for other (3.91), followed by Buffet (3.84), Cafes (3.77), and Dining (3.57).
- **Most common type:** Dining accounts for 110 of 148 records (74.3%) by record count, not customer order volume.
- **Rating distribution:** Ratings span from 2.6 to 4.6, with a mean of 3.63, median of 3.7, and mode of 3.8.
- **Average cost for two:** Highest for Buffet (671.43), followed by other (668.75), Cafes (545.65), and Dining (357.27).
- **Online ordering and ratings:** Records with online ordering average 3.86 (median 3.9) versus 3.49 (median 3.4) for records without it.
- **Without online ordering by type:** Dining has the most records without online ordering (77 marked No vs. 33 marked Yes).

## Conclusion

Dining is the largest category and has the highest total votes, while Buffet has the highest average cost for two. The other category has the highest mean rating across few records, table booking is uncommon, and online-ordering availability is associated with higher ratings in this sample. Because these results describe the 148 supplied records, they should not be generalized to all Zomato restaurants.
