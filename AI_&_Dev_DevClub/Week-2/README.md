# WEEK-2 Submission

## OVERVIEW
This project predicts the number of likes a tweet will receive based on its content, and user/company features using Machine Learning

##  Week 2: WHAT I DID

### Advanced Features
- 'LabelEncoder' used on 'inferred company'
- more parameters like 'has_hashtag', 'has_url', 'day_of_week_num','company_avg_likes','user_avg_likes'
- TF-IDF score ('tfidf_sum') from tweet content
- Data was also scaled
- The model was tested to find diff rmse values by using different combinations of hyperparameters [different number of trees and different depths]to find diff rmse values by using different combinations of hyperparameters 

### Final Feature Set
- 'word_count', 'char_count', 'has_media', 'hour', 'sentiment','company_encoded', 'day_of_week_num', 'has_hashtag', 'has_url','company_avg_likes', 'user_avg_likes', 'tfidf_sum'

### Modeling
- Models tested:
  - `RandomForestRegressor` [ Best with R² ≈ 0.89 ]
  - `LinearRegression`
  - `LGBMRegressor`
  - `MLPRegressor`
- Metrics: RMSE, R²

### Best Model:
- `RandomForestRegressor` with:
  - `n_estimators=100`, `max_depth=10`
  - R² ≈ **0.894**

## To check API running via POSTMAN 
- Trained model saved as `like_predictor.pkl`
- Flask server (`api.py`) exposes POST endpoint:

## 🔗 Quick Access Links

| Resource | Link |
|----------|------|
| Notebook | [Google Colab Notebook](https://colab.research.google.com/drive/1x-3vGGfoMwRre7DOZBjpa4p0Q1me2hdu?usp=sharing) |
| Cleaned Excel Data | [Google Sheets](https://docs.google.com/spreadsheets/d/1IWoYfs4bDkBEnJPCCXHtWc27Xp4xGYE_/edit?usp=sharing&ouid=115952926680497574269&rtpof=true&sd=true) |
| Trained Model (.pkl) | [Google Drive](https://drive.google.com/file/d/14Yy7pBZU0-sT4wKS093C4ol6TOQC96Eo/view?usp=sharing) |
| Working API Code | [Colab API Notebook](https://colab.research.google.com/drive/1OG08iquL0wUn_j7Pe7N-iM5chvtJdUUT?usp=sharing) |

### `/predict`
**Input (JSON):**
```json
{
  "word_count": 12,
  "char_count": 78,
  "has_media": true,
  "hour": 15,
  "sentiment": 0.25,
  "company_encoded": 4,
  "day_of_week_num": 3,
  "has_hashtag": 1,
  "has_url": 0,
  "company_avg_likes": 84.2,
  "user_avg_likes": 102.5,
  "tfidf_sum": 3.57
}
predicted likes came out to be 14913.







