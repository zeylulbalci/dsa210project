# Final Report: Predicting Movie Box Office Success Through Online Engagement Metrics

## 1. Introduction

With the expansion of digital media platforms, the way films gain traction has changed significantly. Platforms such as YouTube and IMDb enable audiences to engage with movie content before and after release by watching trailers, liking and commenting on videos, and submitting ratings and reviews. This project explores whether such engagement can be used as a predictor of a film’s box office success.

The central aim of the project is to assess whether metrics such as YouTube trailer views, likes, comments, and IMDb ratings and vote counts have statistically significant relationships with movie revenue. By identifying patterns in this data, the findings may support more informed marketing, distribution, and production strategies in the entertainment industry.

## 2. Data Collection and Preparation

Data was collected from four main sources. YouTube’s Data API was used to gather information on trailer engagement, including view count, like count, and comment count. IMDb’s official datasets provided movie-level ratings and total vote counts. A dataset from Kaggle supplied gross box office revenue figures for films released in 2023 and 2024. Additionally, data from TMDB was used to enrich the dataset with budget, runtime, popularity, and genre-related information.

A series of data cleaning and preprocessing steps were applied. Currency and numeric formats were normalized (e.g., converting "$1,000,000" to 1000000). A clean_title field and standardized Year column were created to enable accurate merging across datasets. Duplicates were removed, and rows with critical missing data—such as gross revenue, budget, or runtime—were dropped.

New features were also derived to improve the analytical depth of the dataset. These include log-transformed revenue (LogGross), engagement ratios (LikeRatio, CommentRatio, VoteRatio), and binary indicators for genre presence (e.g., is_action, is_comedy, is_drama). After cleaning and feature engineering, the resulting dataset consisted of approximately 120 rows and 15 columns.

## 3. Exploratory Data Analysis (EDA)

A set of exploratory visualizations was created to examine correlations and distributions within the data. A correlation heatmap revealed which features most strongly related to box office performance. Scatter plots were used to visualize the relationship between gross revenue and YouTube or IMDb metrics. Histograms were generated to understand the distribution of variables such as IMDb ratings, revenue, and like ratios.

Among the most notable findings was the strong positive correlation between IMDb vote count and gross revenue. The like ratio (likes/views) also showed a moderately positive correlation with revenue. Budget and gross revenue were positively correlated, though the distribution was heavily skewed due to a few outlier blockbusters.

## 4. Supervised Learning – Regression

A linear regression model was developed to predict log-transformed gross revenue (LogGross) using a combination of production and engagement features. These features included budget, runtime, vote average, vote count, trailer views, likes, engagement ratios, and genre indicators.

The regression model performed reasonably well. The R² score was approximately 0.62, indicating that the model explains about 62% of the variance in revenue. The mean absolute error (MAE) was about 0.31 in log units, corresponding to an average prediction error of ±35%. The root mean squared error (RMSE) was around 0.41.

The results indicate that IMDb and YouTube metrics have significant predictive value. However, the linear model tended to underpredict exceptionally high-grossing films. This suggests that non-linear models—such as decision trees or gradient-boosted methods like XGBoost—may offer improved performance in future work. A scatter plot of actual versus predicted log revenue visually confirmed this trend.

## 5. Supervised Learning – Classification

A classification task was also implemented to predict whether a movie would be a financial "hit." For this purpose, hits were defined as the top 25% of films based on revenue. A RandomForestClassifier was used, with the same features from the regression model.

The classifier achieved an overall accuracy of 89%. Precision for correctly identifying hits was perfect (1.00), meaning no false positives occurred. However, recall for hits was moderate (0.57), indicating that the model missed approximately 43% of actual hits.

This pattern shows that the model is conservative in labeling movies as hits, which can be advantageous in contexts where false positives are costly—such as allocating high marketing budgets or funding high-risk productions.

## 6. Conclusion

This project demonstrates that online engagement metrics—specifically those from YouTube and IMDb—can provide meaningful signals about a movie’s commercial potential. The linear regression model captured the underlying trends between engagement and revenue, while the classifier accurately distinguished high-performing films with minimal false positives.

These findings confirm the hypothesis that digital attention translates into financial outcomes. As such, studios and marketers can incorporate engagement metrics into forecasting tools and greenlighting decisions. Future work may explore the use of nonlinear models, additional variables such as release timing or sequel status, and time-series tracking of engagement to refine predictions further.

