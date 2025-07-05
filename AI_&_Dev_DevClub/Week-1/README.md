# Week 1 Submission

## Overview
This notebook is part of Week 1 of the CAIC Summer of Tech 2025 (AI & Dev Track).  

## What I Did
### Data Cleaning
- Loaded the dataset from Google Drive.
- Removed rows with missing values in key columns ('content', 'username', 'inferred company', 'likes').
- Filled missing values in the 'media' column with 'no_media'.
- Created a new binary column 'has_media' to indicate whether a post has media or not.
- Cleaned and normalized the 'content' column (lowercased and stripped).
- Converted the 'date' column to datetime format.

### Feature Extraction
- Extracted 'hour' and 'day_of_week' from the datetime column.
- Computed 'word_count' and 'char_count' for each post's content.
- Generated a 'sentiment' score.

### Exploratory Data Analysis (EDA)
- Plotted the distribution and boxplot of likes.
- Visualized how average likes vary with hour of day and day of the week.
- Created a scatter plot of sentiment vs. likes.

### Saved Cleaned Data
- Exported the cleaned and feature-enriched dataset to a new Excel file:  
  `Cleaned_behaviour_data.xlsx`
  
## Reflections
Week 1 was mostly about getting started — loading data, cleaning it, and understanding its structure.  
EDA gave initial insights into what features might be useful, such as:
- Posting time
- Sentiment
- Word count
Bonus tasks were also briefly explored

## Notebook Link
https://colab.research.google.com/drive/1x-3vGGfoMwRre7DOZBjpa4p0Q1me2hdu?usp=sharing

## Excel Link
https://docs.google.com/spreadsheets/d/1IWoYfs4bDkBEnJPCCXHtWc27Xp4xGYE_/edit?usp=sharing&ouid=115952926680497574269&rtpof=true&sd=true





## 👤 Author

Madhusmita  Talukdar
2024CS10253
CAIC Summer of Tech 2025 – Week 1
