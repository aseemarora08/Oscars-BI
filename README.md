# OSCARS: Analysis and Visualization Documentation
## Question:
*What historical trends and patterns emerge among Oscar Best Picture nominees and winners in the past century?*

## Data Source:
Oscar Best Picture Movies dataset - https://www.kaggle.com/datasets/martinmraz07/oscar-movies/data

We used this data because the dataset offers a wide range of variables useful in identifying and analyzing trends in past Oscar Best Picture nominations and wins. The dataset includes data from the past century, which can be used in a comparative analysis to identify patterns and shifts in the film industry over time according to the characteristics of Oscar-nominated films across different decades.

## Main Variables:
Film (Title of Film), Main Genre (Primary Movie Genre), Oscar Year (Year of Award Show), Content Rating (G, PG, PG-13, R), Production Company (Producer/Studio), Movie Time (Film Duration), Award (Nominee, Winner)

## Data Transformations:
The data preprocessing steps you've outlined provide a clear understanding of how you cleaned and enhanced the dataset. Here's a summary of each step:

1. **Data Cleansing:**
   Eliminated empty/null values in the dataset to ensure data integrity.
   Addressed inconsistencies, including redundant entries and misspelled fields, to enhance data accuracy.

2. **Created Main Genre Column:**
   Recognized the presence of multiple genres in the Movie Genres column.
   Introduced a new column named "Main Genre" to highlight the primary genre for Best Picture nominees and winners, facilitating better analysis and categorization.

3. **Created IMDB Rating (100) Column:**
   Adapted the IMDB rating scale from 0-10 to a 0-100 scale.
   Implemented this transformation by introducing a new column and multiplying the existing IMDB rating field by 100.

4. **Difference Between IMDB Ratings and Rotten Tomatometer Ratings:**
   Added a new column to the dataset that computes the absolute value of the difference between IMDB Ratings and Rotten Tomatometer Ratings.
   This addition aims to explore the relationship between rating disparities and the likelihood of films being nominated or winning an Oscar in the past.

These steps collectively contribute to the improvement of the dataset's quality, making it more suitable for insightful analysis and meaningful conclusions. The transformations, such as creating a main genre column and standardizing rating scales, enhance the dataset's usability for exploring trends and patterns related to Oscar-nominated films.

## Visualizations:
*Note that an “Awarded” film can either be an Oscar nominee or winner. We’ve added a slicer to filter results based on nominees versus winners.
1. **Most Common Genres Awarded:**
Utilized a treemap to visually represent the prevalence of awarded movie genres based on the number of films recognized.

2. *Production Companies with the Most Awarded Films:**
Presented a clustered bar chart to highlight the top 5 (including a tie on 5th and 6th place) most successful production companies. The categorization is based on the number of movies nominated for the Oscars, with an additional breakdown by Content Rating.

3. **Comparison of IMDb and Tomatometer Ratings on Awarded Films:**
Developed a scatter plot to showcase the relationship between IMDb (fan ratings) and Rotten Tomatoes’ Tomatometer (critics' ratings). The plot effectively illustrates the number of movies nominated based on the difference between these two rating systems.

4. **Average Duration of Awarded Films Over the Past Century:**
Constructed a line chart that spans a century, grouping average movie durations into ten-year buckets. This visualization provides insights into the historical trends in the length of films recognized by the Oscars.

5. **Number of Films Awarded Based on Film Duration:**
Employed a histogram to visualize the distribution of movie durations and the corresponding count of awarded films. This histogram offers a snapshot of the films most likely to be nominated or win an Oscar, based on their duration.

6. **Content Rating Distribution:**
Designed a doughnut diagram to represent the proportional distribution of each content rating category that has been nominated for the Oscars over the past century. This visualization provides a quick overview of the content rating landscape in the history of Oscar-nominated films.

## Conclusion: 
Analyzing Oscar awarded films based on our main variables, it is concluded that Drama films by the Warner Bros. production company, between a 120-140 minute duration, with a content rating ‘R’, along with an IMDb and Tomatometer disparity between 10-20 points are most likely to be an Oscar nominee or winner for Best Picture.
