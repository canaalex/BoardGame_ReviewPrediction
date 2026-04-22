# Board Game Rating Analysis

## Overview  
This project investigates the factors influencing board game ratings using a regression-based approach. The objective is to understand whether structural game attributes (such as playtime and player count) or user engagement metrics (such as ownership and wishlist counts) better explain variations in ratings.

---

## Dataset  
The dataset contains over **81,000 board games**, including features such as:
- Game characteristics (playtime, complexity, number of players)  
- User engagement metrics (owners, wishlists, comments)  
- Rating-related variables  

---

## Data Preprocessing  
- Removed entries with invalid values (e.g., non-positive years, zero playtime)  
- Dropped irrelevant features such as IDs and names  
- Excluded `bayes_average_rating` to prevent data leakage  
- Retained only meaningful numerical features for modelling  

---

## Exploratory Analysis  
Correlation analysis revealed that:
- **Game complexity (`average_weight`)** has the strongest positive relationship with ratings  
- **User engagement metrics** show moderate correlation  
- **Playtime and player count** have minimal influence  

---

## Model  
A **Linear Regression model** was used as a baseline due to its interpretability.

**Performance:**
- R² Score: **0.30**  
- Mean Squared Error: **5.79**

---

## Key Insights  
- Players tend to favour **strategically complex games** over simpler ones  
- **Popularity does not strongly determine quality**, as engagement metrics show only moderate influence  
- Structural features like **playtime and player count have negligible impact** on ratings  
- A significant portion of rating variability is driven by **subjective factors**

---

## Limitations  
- The model explains only ~30% of rating variance  
- Important qualitative aspects (e.g., theme, design, player experience) are not captured  
- Linear regression may not capture non-linear relationships  

---

## Future Work  
- Incorporate **text analysis of user reviews**  
- Experiment with **non-linear models** (e.g., Random Forest, XGBoost)  
- Include richer gameplay and design-related features  

---

## Conclusion  
The findings suggest that players prioritise **depth and complexity** over structural attributes such as duration or player count, while engagement metrics reflect popularity rather than intrinsic quality. This highlights the importance of subjective experience in shaping user ratings.
