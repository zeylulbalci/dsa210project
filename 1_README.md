## 1. Abstract
   
In this project, I will explore the relationship between online popularity and a movie’s commercial success. I will specifically focus on two major platforms — YouTube and IMDb — to investigate whether publicly available data from these sites can help predict how well a film performs at the box office. I believe that analyzing user interactions with trailers on YouTube, along with audience ratings and vote counts on IMDb, will offer meaningful insights into a movie’s popularity and financial outcome. The results of this study may help reveal how online engagement translates into real-world performance.

## 2. Introduction
   
With the rise of digital platforms, the way movies are promoted and received by audiences has changed significantly. Today, people discover and discuss films online — especially through platforms like YouTube, where trailers are shared, and IMDb, where viewers rate and review them. In this project, I aim to investigate whether YouTube trailer metrics such as views, likes, and comments, along with IMDb ratings and vote counts, can be used to estimate how successful a movie will be financially. My ultimate goal is to understand whether these online interactions reflect — or even influence — box office outcomes.

## 3. Data Collection and Preparation
   
To conduct this study, I will collect data from three main sources. First, I will use the YouTube API to gather information on trailer engagement for each film, including the number of views, likes, and comments. Second, I will use IMDb’s official datasets to obtain average ratings and the number of votes per movie. Third, I will include a box office dataset that provides gross revenue figures. If possible, I will also enrich the dataset using TMDB to add information like budget, genres, and runtime. After collecting all data, I will clean and merge the datasets based on movie titles and release years. I will convert numerical formats, remove inconsistencies, and standardize the features to prepare them for analysis. Although I initially considered incorporating Twitter sentiment data, I will exclude it due to technical limitations.

## 4. Methodology
   
Once I compile a clean and complete dataset, I will begin with exploratory data analysis (EDA) to understand general patterns and trends. I will compute correlation matrices to examine how features such as YouTube engagement and IMDb metrics relate to box office gross. I will also create visualizations like scatter plots and heatmaps to further explore these relationships. After the EDA, I plan to implement machine learning models, including a regression model to predict gross revenue and a classification model to identify box office hits. All steps will be performed in Python using packages such as pandas, matplotlib, seaborn, and scikit-learn.

## 5. Limitations and Future Work
    
There are some expected limitations in this project. First, I will not be able to include Twitter sentiment analysis, which could have provided deeper understanding of audience opinion. Second, movie revenue is influenced by many external factors that are not represented in the dataset — such as marketing strategies, release timing, or franchise popularity. Moreover, IMDb ratings can sometimes be biased due to fan enthusiasm or manipulation. In the future, I could expand the analysis by incorporating data from platforms like TikTok or Instagram, and by applying time-series techniques to model changes in audience engagement over time.

## 6. Conclusion
    
Through this project, I hope to understand whether online interactions — particularly on YouTube and IMDb — are associated with a movie’s financial success. I expect to find that films with higher engagement on these platforms tend to perform better at the box office. While these metrics may not capture the full picture, they can serve as valuable indicators of public interest. Ultimately, this study aims to demonstrate that online popularity data can be used as part of a broader framework to anticipate commercial performance and support marketing or production decisions.
