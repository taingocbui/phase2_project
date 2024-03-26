# Movie Data Exploratory Analysis

Author: Tai Ngoc Bui <br>
Date Completion: March 24th, 2024

## 1.Business Understanding
This data exploratory project focuses on analyzing characteristics of successful movies at the box office to support the company's strategic investment in the movie industry. The goal is to gain valuable insights contributing to movie production success and provide meaningful recommendations to major stakeholders of the investments.

## 2.Data Understanding
The dataset used in this analysis extracted from various different movie sources including:

* [IMDb](https://www.imdb.com/)
* [The Numbers](https://www.the-numbers.com/)
* [TheMovieDB](https://www.themoviedb.org/) <br>

As these datasets were collected from different sources, they have different formats. While The Movie DB and the Numbers datasets are compressed as CVS files, the IMDb, the largest dataset among the three, is stored within a SQLite database.<br>

![IMDb database structure](https://github.com/taingocbui/phase2_project/blob/main/photos/movie_data_erd.jpeg)

These datasets not only contain movies' information on their casts, directors, budget, and revenues, etc. but also the public opinions regarding the movies' success such as ratings and votes.


## 3. Objectives
* Explore and analyze three different datasets to identify general trends in the movie industry, and the major factors that contribute to the sucess of a movie.
* Provide data-driven evidence to support confidence in the strategic investment and the best strategies to minimize the overall investment risks.
* Identify a list of potential directors based on their track records to ensure the success of stakeholders' investment in the movie industry.

## 4. Key Questions
With this project, I will address specific questions such as:
* What specific measure should be used to compare the sucess of movies and their production team?
* Would it be possible to reduce investment risk if we prioritizing certain movies' genres or release month?
* Who should be prioritized to be our studios' lead directors?
* What should we learn from the success of past blockbusters?

## 5. Data Cleaning
As data is extracted from different sources, each dataset requires different cleaning techniques. As IMDb has the largest dataset among the three sources, it also has the most amount of Nan values and duplicates. As I want to use this dataset to analyze how directors contribute to movies' success, I decide to only keep records in which the person is still alive and the category column is not Nan. With quantitative features such as average ratings and number of votes, I replace Nan values with zero, while the Nan values in runtime minute are replaced with the runtime minutes' mode. <br>
Unlike IMDb dataset, the Numbers' and the Movie DB's datasets do not have any Nan values or duplicates. However, all quantitative features in the Numbers' dataset such as production budget, and gross revenue are all formatted as string type. To convert these features into float type, I need to remove all special characters $ sign from these strings. On the other hand, the Movie DB's dataset has all movies' genres stored as an id code. Though it looks like data in this genre id column is stored as lists; in fact it is all formatted as string type. As a movie can have multiple different genres, my solution for this column is to split them into multiple columns, each column represent a genre type. If the movie is assigned with a certain genre, that genre type will show as 1 for that column, else will be 0.

## 6. Exploratory Data Analysis
For this project, I decided to use Return on Investment (ROI) as the main measure to compare the sucess of various movies, directors, and producers. 

# Conclusion

## Limitations

## Recommendations