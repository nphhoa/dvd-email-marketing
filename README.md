# DVD Rental CO Email Marketing Analytics

Personalized customer emails based off marketing analytics is a winning formula for many digital companies, and this is exactly the initiative that the leadership team at DVD Rental Co has decided to tackle.

This project been asked to support the customer analytics team at DVD Rental Co who have been tasked with generating the necessary data points required to populate specific parts of this first-ever customer email campaign.

## 🛠️ Requirements
The marketing team have shared a draft of the email they wish to send to their customers.

<img src="/images/email-template.png" width=50% height=50%>

### 📋 Requirement #1: Top 2 Categories

For each customer, I need to identify the top 2 categories for each customer based off their past rental history. These top categories will drive marketing creative images as seen in the travel and sci-fi examples in the draft email.

### 📋 Requirement #2: Category Film Recommendations

The marketing team has also requested for the 3 most popular films for each customer’s top 2 categories. There is a catch though - I cannot recommend a film which the customer has already viewed.

If there are less than 3 films available - marketing is happy to show at least 1 film.

Any customer which do not have any film recommendations for either category must be flagged out so the marketing team can exclude from the email campaign.

### 📋 Requirement #3 & #4: Individual Customer Insights

The number of films watched by each customer in their top 2 categories is required as well as some specific insights.

For the 1st category, the marketing requires the following insights (requirement 3):
1. How many total films have they watched in their top category?
2. How many more films has the customer watched compared to the average DVD Rental Co customer?
3. How does the customer rank in terms of the top X% compared to all other customers in this film category?

For the second ranking category (requirement 4):
1. How many total films has the customer watched in this category?
2. What proportion of each customer’s total films watched does this count make?

### 📋 Requirement #5: Favorite Actor Recommendations

Along with the top 2 categories, marketing has also requested top actor film recommendations where up to 3 more films are included in the recommendations list as well as the count of films by the top actor.

I have been given guidance by marketing to choose the actors in alphabetical order should there be any ties - i.e. if the customer has seen 5 Brad Pitt films vs 5 George Clooney films - Brad Pitt will be chosen instead of George Clooney.

The same logical business rules apply - in addition any films that have already been recommended in the top 2 categories must not be included as actor recommendations.

If the customer doesn’t have at least 1 film recommendation - they also need to be flagged with a separate actor exclusion flag.

## 📂 Data Analytics Flow

### Problem
[![View Problem Folder](https://img.shields.io/badge/View-Problem_Folder-b11226?style=for-the-badge&logo=GITHUB)](Problem.ipynb)

### Exploration
Before diving straight into solution mode for the business requirements, I need to take a look at the data with EDR (Entity-Relationship Diagrams) to identify different data relationships between tables. The EDR of these datasets can be viewed as below:

<img src="/images/ERD full.png">

I’ve labeled each of our spotlight tables from 1 through to 7 so I can keep track of where I am as I explore the available data. Therefore, the first section will cover the data inspection process of these tables in order to find out the best JOIN type that will be the most suitable for the later problem solving stage.

[![View Exploration Folder](https://img.shields.io/badge/View-Exploration_Folder-b11226?style=for-the-badge&logo=GITHUB)](/Exploration.ipynb)
 
### Analysis 
Now that I’ve identified the key columns and highlighted some things I need to keep in mind when performing some table joins for my data analysis - next exciting step is to join them together.

[![View Analysis & Report Folder](https://img.shields.io/badge/View-Analysis_&_Report_Folder-b11226?style=for-the-badge&logo=GITHUB)](/Analysis%20&%20Report.ipynb)

### Report
This is what out final input looks like:

<img src="/images/email-output.png" width=50% height=50%>
