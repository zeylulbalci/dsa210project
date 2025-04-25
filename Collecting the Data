1. Collecting the Data

In this project, I collected data from three main sources in order to build a unified dataset for further analysis: Kaggle (box office data), YouTube (trailer engagement), and IMDb (audience rating and vote count). My objective was to combine information from these platforms into a structured format that could help evaluate the relationship between online engagement and box office success.

To begin, I used a Kaggle dataset that included the titles, release years, and gross revenue of movies released in 2023 and 2024. The gross revenue values were formatted with currency symbols and commas, so I cleaned this column by removing these characters and converting the values into numeric format. I also filtered the dataset to keep only movies from the desired years, ensuring consistency across sources.

For YouTube data, I utilized the YouTube Data API to collect trailer-related statistics. I constructed search queries by combining each movie title with its release year and the keyword "trailer", and retrieved the most relevant video for each query. From the corresponding videos, I collected view counts, like counts, and comment counts. Due to API quota limitations, I divided the full list of movies into batches of 100 and collected the data incrementally over time. In some cases, missing entries were added manually to preserve order and completeness.

The third component of the dataset came from IMDb. I downloaded the official IMDb datasets and extracted the rating and vote count for each movie. Since the movie titles in the box office dataset and IMDb datasets were not always written identically, I used fuzzy string matching techniques to find the most accurate matches. I also cleaned the movie titles by removing special characters and matching them based on both title and release year. Once the matches were confirmed, I merged the IMDb data with the existing dataset.

By the end of the data collection process, I had created a single dataset containing key information for each movie: the title, release year, gross revenue, YouTube trailer engagement statistics (views, likes, comments), and IMDb rating and vote count. This prepared dataset will be the foundation for the exploratory data analysis and hypothesis testing in the next stages of the project.


