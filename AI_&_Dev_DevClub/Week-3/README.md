#  Week 3 Submission

## OVERVIEW
This week I extended the tweet generation system to make it smarter, more customizable, and brand-ready.
I added sentiment-based smart tweet generation, industry-based formatting, brand voice control, and even used a trained ML model to predict the number of likes a tweet might get. I also experimented with GPT-2 based tweet generation as a bonus!

## WEEK3 - What Did I Do

- Template-based tweet generation (basic & advanced)
- Integration with ML model to predict tweet likes
- Feature extraction using TF-IDF + sentiment + media
- Smart Tweet Generator (Bonus 2): Sentiment-aware tweets
- Branded Tweet Generator (Bonus 3): Adjust tone by industry & brand voice
- AI Tweet Generator (Bonus 1): GPT-2 based continuation (commented)

### Files & Links

| File Name               | Link |
|-------------------------|------|
| `tweet_generator.py`    | [Open in Colab](https://colab.research.google.com/drive/1hWeeLENnJxhjxXe-dgCPUdmE34xtj4Wu?usp=sharing) |
| `app_generator.py`      | [Open in Colab](https://colab.research.google.com/drive/1QMa0DpQ7kCnzQ6ZBKyxLWy7w_7Lhvuye?usp=sharing) |
| `bonus_ai_generator.py` | [Open in Colab](https://colab.research.google.com/drive/1hy_OuoYYnslWx7iKEtU5aI2NJkJgaRV0?usp=sharing) |
| `tfidf_vectorizer.pkl`  | [Download](https://drive.google.com/file/d/1qT5LKTgMnDfdQGhp7IdSE0BS4VRPUEle/view?usp=sharing) |

## How It Works

###  Basic Tweet Generator
Uses predefined templates like:
- `announcement`, `question`, `product launch`, `event`, `achievement`, `hiring`, `giveaway`, etc
Each tweet is generated using dynamic fields like `{company}`, `{topic}`, `{message}`, etc.

### Smart Tweet Generator (Bonus 2)
- Chooses between positive, negative, and neutral templates
- Controlled by `sentiment_target` value
- Adds media tag if required

### Branded Tweet Generator (Bonus 3)
- Customizes tone by:
  - Industry: tech, food, fashion, etc.
  - Voice: casual, professional, playful
- Adds branding-specific emojis and styles

## Flask API (in `app_generator.py`)

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/generate_basic_tweet` | POST | Generates tweet using all parameters & predicts likes |
| `/generate_smart_tweet` | POST | Generates tweet based on sentiment score |
| `/generate_branded_tweet` | POST | Generates tweet based on industry & brand voice |
| `/health` | GET | Returns status of API |

## Author
Madhusmita Talukdar
2024CS10253

