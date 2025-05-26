#1. Abstract
   
In this project, I aim to explore the relationship between online popularity and a movie’s commercial success. I will specifically focus on two major platforms — YouTube and IMDb — to see if the data available on these sites can help predict how well a film performs at the box office. I believe that analyzing user interaction with trailers on YouTube, along with audience ratings and vote counts on IMDb, can offer insights into a movie’s popularity and financial outcome. The results of this project may help understand how online engagement translates into real-world performance.

2. Introduction
   
With the rise of digital platforms, the way movies are promoted and received by audiences has changed significantly. Today, people discover and discuss movies online — especially through platforms like YouTube, where trailers are published, and IMDb, where viewers rate and review films. In this project, I want to investigate whether YouTube trailer metrics such as views, likes, and comments, along with IMDb ratings and vote counts, can be used to estimate how successful a film will be financially. My main goal is to understand whether these forms of online interaction reflect or even influence box office performance.

3. Data Collection and Preparation
   
To conduct this study, I will collect data from three main sources. First, I will use the YouTube API to gather information on trailer engagement for each movie, including the number of views, likes, and comments. Second, I will use IMDb’s official datasets to obtain average ratings and the number of votes per film. Third, I will include a box office dataset that provides the gross revenue for a wide selection of films. After collecting all the data, I will clean and merge these datasets based on movie titles and release years. I will also convert number formats, remove inconsistencies, and standardize the data to prepare it for analysis. Although I initially considered including Twitter sentiment analysis, I decided to exclude it due to technical limitations in data access.

4. Methodology
   
Once I have a clean and complete dataset, I will begin by performing exploratory data analysis (EDA). I will use correlation analysis to see how strongly each variable — such as IMDb rating, number of votes, YouTube views, likes, and comments — is related to box office gross. I plan to create visualizations such as scatter plots and heatmaps to better understand the patterns in the data. I will also use histograms to observe how IMDb ratings are distributed across the sample. All analysis will be conducted using Python, with libraries like pandas, matplotlib, and seaborn. This approach will help me evaluate whether online engagement metrics are meaningful predictors of financial success.

5. Limitations and Future Work
    
There are some limitations to this project that I am aware of. First, I will not be able to include Twitter data or sentiment analysis, which could have added another layer of understanding. Also, box office revenue is influenced by many external factors that are not present in my dataset — such as marketing budgets, franchise popularity, seasonal trends, and global distribution. Additionally, IMDb ratings might not always be objective due to things like early fan enthusiasm or coordinated rating campaigns. In the future, I could improve this project by including data from other platforms like TikTok and Instagram, or by tracking audience engagement over time using time-series analysis.

6. Conclusion
    
Through this project, I aim to understand whether online interactions — particularly those on YouTube and IMDb — are connected to how well a film performs at the box office. I expect to find that films with more YouTube engagement and stronger IMDb presence will tend to earn more revenue. Although these platforms do not tell the whole story, I believe they provide valuable signals about public interest. By the end of this study, I hope to show that online data can be used as part of a larger strategy to anticipate the financial performance of films and make more informed marketing or production decisions.
