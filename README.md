# Amazon-Prime-Dataset-Project

# Movie Dataset Analysis and Predictive Modeling

## Table of Contents
1. [Introduction](#introduction)
2. [Data Overview](#data-overview)
3. [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Correlation Analysis](#correlation-analysis)
6. [Predictive Modeling](#predictive-modeling)
7. [Conclusion](#conclusion)
8. [Future Work](#future-work)


## Introduction
The aim of this project is to analyze a movie dataset to understand trends and build a predictive model for IMDb ratings. The analysis will help identify key factors that influence movie ratings and how this information can be leveraged for better insights.

## Data Overview
The dataset contains movie information with the following columns:
- **title**: Name of the movie
- **type**: Type of media (e.g., movie)
- **genres**: Genres of the movie
- **releaseYear**: Year of release
- **imdbId**: IMDb ID for the movie
- **imdbAverageRating**: IMDb average rating
- **imdbNumVotes**: Number of votes on IMDb
- **availableCountries**: Countries where the movie is available

**Initial Observations**:
- Basic data exploration indicates some missing values in columns such as `releaseYear` and `imdbNumVotes`.
- The dataset includes both numerical and categorical data types.

## Data Cleaning and Preprocessing
- **Handling Missing Values**: Missing values in `releaseYear` were filled with the median, and `imdbNumVotes` were filled with zero.
- **Data Type Adjustments**: Converted `releaseYear` to integer and `imdbNumVotes` to integer for consistency.
- **Outlier Detection**: Outliers in `imdbAverageRating` were inspected but not removed as they represent valid data points.
- **Feature Engineering**: No additional features were engineered at this stage, but future iterations may include feature extraction from `genres`.

## Exploratory Data Analysis (EDA)
Visualizations and analyses performed include:
- **Distribution of IMDb Ratings**: Histogram plot showing the distribution of movie ratings.
- **Movies Released Per Year**: Bar chart visualizing the number of movies released annually.
- **Most Common Genres**: Bar plot highlighting the most frequently occurring movie genres.

**Key Findings**:
- The distribution of IMDb ratings is skewed towards higher values.
- The number of movies released has fluctuated over the years, with notable peaks and declines.
- Certain genres, such as `Drama` and `Comedy`, are more prevalent.

## Correlation Analysis
A correlation matrix was plotted to examine relationships between numerical features such as `releaseYear`, `imdbAverageRating`, and `imdbNumVotes`.

**Insights**:
- Weak positive correlation between `imdbNumVotes` and `imdbAverageRating`.
- No strong correlation between `releaseYear` and `imdbAverageRating`, suggesting ratings are not time-dependent.

## Predictive Modeling
### Model Selection
A linear regression model was chosen to predict IMDb ratings using `releaseYear` and `imdbNumVotes` as features.

### Data Splitting
- **Training Set**: 70% of the data
- **Testing Set**: 30% of the data

### Model Training and Evaluation
- **Model Performance Metrics**:
  - **Mean Squared Error (MSE)**: [Insert MSE value]
  - **R-squared**: [Insert R-squared value]

**Limitations**:
The linear regression model has limited predictive power, indicating that more complex models or additional features may be needed for better performance.

## Conclusion
The project successfully explored the dataset and built a baseline predictive model for IMDb ratings. Key insights include:
- The number of votes impacts IMDb ratings more than the year of release.
- Popular genres such as `Drama` and `Comedy` dominate the dataset.

## Future Work
- **Model Improvements**: Explore more complex algorithms (e.g., Random Forest, Gradient Boosting).
- **Feature Expansion**: Include `genres` and `availableCountries` for richer modeling.
- **Additional Data**: Integrate movie budget, box office revenue, and critic reviews for better prediction accuracy.

