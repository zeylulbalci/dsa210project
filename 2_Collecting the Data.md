## Collecting the Data

In this project, I collected data from four main sources in order to build a unified dataset for further analysis: Kaggle (box office data), YouTube (trailer engagement), IMDb (audience rating and vote count), and TMDB (enrichment metadata such as budget, revenue, runtime, genres, popularity). My objective was to combine information from these platforms into a structured format that could help evaluate the relationship between online engagement and box office success.

To begin, I used a Kaggle dataset that included the titles, release years, and gross revenue of movies released in 2023 and 2024. The gross revenue values were formatted with currency symbols and commas, so I cleaned this column by removing these characters and converting the values into numeric format. I also filtered the dataset to keep only movies from the desired years, ensuring consistency across sources.

For YouTube data, I utilized the YouTube Data API to collect trailer-related statistics. I constructed search queries by combining each movie title with its release year and the keyword "trailer", and retrieved the most relevant video for each query. From the corresponding videos, I collected view counts, like counts, and comment counts. Due to API quota limitations, I divided the full list of movies into batches of 100 and collected the data incrementally over time. In some cases, missing entries were added manually to preserve order and completeness.

The third component of the dataset came from IMDb. I downloaded the official IMDb datasets and extracted the rating and vote count for each movie. Since the movie titles in the box office dataset and IMDb datasets were not always written identically, I used fuzzy string matching techniques to find the most accurate matches. I also cleaned the movie titles by removing special characters and matching them based on both title and release year. Once the matches were confirmed, I merged the IMDb data with the existing dataset.

Finally, I enriched the dataset using TMDB’s public dataset, which contains additional metadata for thousands of films. This dataset was large, so I processed it in chunks to avoid memory overload. From TMDB, I extracted key features such as production budget, revenue, runtime, popularity, vote average, vote count, and genres. I created a clean_title column by standardizing the movie titles (lowercase, no punctuation), and also extracted the release year from the release_date column. I then merged the TMDB data with my previously prepared dataset by matching on both clean_title and release_year. In cases where multiple matches existed, I retained only the most relevant one. After this step, I dropped any irrelevant columns and ensured that numeric columns were properly typed.

By the end of the data collection process, I had created a single enriched dataset containing the following key information for each movie:

Title and release year

Box office gross revenue (from Kaggle)

YouTube trailer statistics (views, likes, comments)

IMDb rating and vote count

TMDB metadata: budget, revenue, runtime, genres, popularity, vote average, vote count

This prepared and cleaned dataset formed the foundation for the exploratory data analysis, hypothesis testing, and machine learning models developed in the following phases of the project.
