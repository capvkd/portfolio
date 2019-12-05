# Investigating Fandango Movie Ratings

### Project Intro

Back in October 2015, Walt Hickey, a data journalist, analyzed movie ratings data from the Fandango website. Hickey looked at 205 movies from 2015 and found that there was a significant discrepency between the rating showed to users and the actual rating based on reviews (found in the page's HTML code). He published his findings in this [article](https://fivethirtyeight.com/features/fandango-movies-ratings/).

In this project, we'll analyze the ratings data from Fandango for more recent movies to determine if Fandango made any changes to the ratings shown to users after the analysis by Hickey was published.

### Data:
- [fandango_score_comparison.csv](https://github.com/fivethirtyeight/data/tree/master/fandango): The original data Walt Hickey analyzed for his article, which he made publicly available on GitHub. We'll use the data he collected to analyze the characteristics of Fandango's rating system previous to his analysis.
- [movie_ratings_16_17.csv](https://github.com/mircealex/Movie_ratings_2016_17): Publicly available movie ratings data for movies released in 2016 and 2017.

### Project Steps

For this project, we are comparing movie ratings before Hickey's analysis (2015) and after. We want to identify any changes in the ratings between the two years and we'll do so using three different approaches.

First, we look at the kernel density plots for each dataset to compare the distributions of ratings accross both years. Then we follow up by creating frequency tables of the ratings in each set. Lastly, we look at the aggregate statistics for each dataset.

We end up identifying a change in the ratings distribution from 2015 to 2016, as observed across the three different approaches we took in the analysis.
