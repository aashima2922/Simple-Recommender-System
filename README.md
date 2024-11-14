# Simple-Recommender-System
Simple Recommender System


**Popular-Item Recommendation System**
This project implements a basic recommendation system that suggests the most popular items to users. It’s a simple, efficient way to recommend items based on overall popularity, making it suitable for scenarios where personalized recommendations are not required or when fallback recommendations are needed.

How It Works
Data Loading:

The system reads data from three main CSV files:
items.csv: Contains information about each item, including categories.
users.csv: Contains information about each user, including their country.
events.csv: Logs user interactions with items, including timestamps.
Training - Calculating Popular Items:

The system identifies the most popular items by counting interactions with each item. These popular items are used as default recommendations.
Session Analysis:

User interactions are grouped into sessions if there’s an 8-hour gap between events for a single user.
Duplicate item visits within a session are removed, and sessions with only one event are excluded.
Various session statistics are calculated, including session count, average events per session, and bounce rates.
Simple Recommendation Method:

The system recommends the top 5 most popular items for each session. This simple approach ensures that popular items are consistently suggested across all sessions.
Evaluation:

The model evaluates recommendations by checking if the target item for each session is among the recommended popular items. A "hit rate" is calculated to measure recommendation accuracy.
Usage
Prepare Data Files: Ensure items.csv, users.csv, events.csv, and sessions.csv are in the same directory as the code.

Output:
The program displays session statistics, the recommended items for each session, and evaluation results showing recommendation accuracy.
