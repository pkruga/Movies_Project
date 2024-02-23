# Movies_Project
![pexels-louis-1200450](https://github.com/pkruga/Movies_Project/assets/91247293/45da2718-ecd4-438a-b8eb-58170c543647)

# Project Overview
For this project, you will use exploratory data analysis to generate insights for a business stakeholder.

# Business Problem
Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

# Execution of Project Tasks
As we're working on a draft document the code will be run first before we make our final presentation. Below is step one: data loading using pandas.

# The Data
We are going to fetch information on movie titles, box office ratings and the box office gross from the follwing files.

* imdb.title.basics
* imdb.title.ratings
* bom.movie_gross

# Methodology
We used the 3 files above for our analysis and added a fourth movie_budgets.csv for budgetary analysis. From our merged data we'll look at the performance at the box office across genres, ratings, and estimated budgets. Our Analysis will cover the following points of interest:

* revenue generated by each movie genre.
* influence of ratings on gross earnings.
* whether release dates affect our gross earnings.

## Data Gathering:
Load the data from the provided CSV files into your Jupyter Notebook using pandas.

## Data Cleaning
Check for data redundancy including, duplicates, and missing values that might affect our data analysis stage. 

### Analysis by Genre
**Genre Analysis**: Analyze the distribution of movie genres and identify the most popular genres. You can calculate the frequency of each genre and visualize it using bar plots.

**Revenue by Genre**: Analyze the relationship between net revenue for different genres. You can calculate average revenue and budget for each genre and visualize it using grouped bar plots or box plots.

### Analysis by Rating
Ratings give us insight into how audience and critics' opinion of a movie affected it's performance in revenue.

**Rating Analysis**: Explore the distribution of movie ratings (averagerating) and identify any trends or patterns. You can create histograms or box plots to visualize the distribution.

**Rating vs. Revenue**: Analyze the relationship between movie ratings and revenue using correlation analysis. We can calculate average revenue for different rating categories and visualize it using box plots or scatter plots.

### Analysis by Release Date
**Release Date Analysis**: Analyze the distribution of movie releases over time and identify any seasonal trends. You can group movies by release year or month and visualize the distribution using line plots or bar plots. We'll use an ANOVA test which will output a test statistic and p-value. 

The p-value indicates the significance of the differences in gross earnings among movies released in different months. A low p-value (< 0.05) suggests that there is a significant difference in gross earnings among months, while a high p-value suggests no significant difference.

These analyses provide numerical insights into the influence of ratings and release dates on gross earnings, complementing the visualizations.

**Budget vs. Revenue Trends Over Time**: Analyze how the relationship between production budget and revenue has changed over time. You can calculate average budget and revenue for different time periods and visualize it using line plots.

# Results

## Analysis by Genre

![image](https://github.com/pkruga/Movies_Project/assets/91247293/7ecc0b41-8bb7-418d-8bcb-3a3c289d3236)

We can see the most popular genres are drama and comedy as per how many films feature each of the genres in the list. 

![image](https://github.com/pkruga/Movies_Project/assets/91247293/0fb0ebd9-89d9-4176-8ddd-ca36e23342f6)

We see that Adventure, Animation, Action, and Sci-Fi are the most popular genres. Showing that they are the most likely to attract audiences.

We see that Adventure, Animation, Action, and Sci-Fi are the most popular genres. Showing that they are the most likely to attract audiences.

These figures contradict our earlier observation of most movies featuring comedy and drama genres proving that they are common but not necessarily popular.

## Analysis by Rating

![image](https://github.com/pkruga/Movies_Project/assets/91247293/bf8bb98f-b0da-4c36-97a3-9c610d0001b9)

Correlation between average ratings and gross earnings: 0.21234671196360377
The correlation coefficient between average ratings and gross earnings is approximately 0.21.

In simple terms, this positive correlation indicates that there is a weak to moderate relationship between the average ratings of movies and their gross earnings.

This means that the audience and critics' rating of a movie does not necessarily affect it's revenue. 
However, it's important to note that the correlation is not very strong, suggesting that other factors besides ratings also play a role in determining the financial success of a movie.

![image](https://github.com/pkruga/Movies_Project/assets/91247293/52c1075d-ac93-4a11-b4dd-b9b2b9bf3172)

Our different genres are rated in a similar range even in combination with other genres, Western and biography are rated higher than most other genres. This can be stated as they are attract positive reviews even when combined with other genres.

![image](https://github.com/pkruga/Movies_Project/assets/91247293/c3bb8b7a-4654-4584-a8b3-75879343f903)

Q1 (25th percentile): 4.2 Median (50th percentile): 6.5 Q3 (75th percentile): 8.8 Interquartile Range (IQR): 4.6000000000000005. These statistics suggest that the movie ratings exhibit variability, with a wide range of ratings observed across the dataset. The median rating of 6.5 indicates that the central tendency of the ratings distribution is around this value, with approximately half of the movies having ratings below 6.5 and the other half having ratings above it.

However note that there are more outliers in the past our Q1 value than our Q3 value. Showing that more movies are rated lower than higher even in our distribution.


## Analysis by Release Date

**ANOVA Test Result**:
F_onewayResult(statistic=1.971510556756346, pvalue=1.0469216871194916e-16)
This indicates that there is a statistically significant difference in gross earnings among movies released in different months. 
The extremely low p-value (1.05e-16) suggests that the differences in gross earnings among months are highly unlikely to be due to random chance alone. 
Therefore, we can conclude that release dates have a significant impact on gross earnings. However, it's important to perform further analysis or consider other factors to understand the specific patterns or trends associated with release dates and gross earnings.

![image](https://github.com/pkruga/Movies_Project/assets/91247293/81563140-4ff0-4b06-9bfb-f595c863c5d8)

![image](https://github.com/pkruga/Movies_Project/assets/91247293/1041823a-ed89-49e1-b8bc-f882d00d1375)

The most likely months that seem to make more money are the spring and Summer months between April and June. This by no means that these months are the best times to release films as we see strong revenue generation in October and November.

# Conclusions
**Genre Popularity and Revenue Generation**:
Adventure, Animation, Action, and Sci-Fi are identified as the most popular genres based on the frequency of movie releases.
These genres are also among the top revenue generators, indicating that they have a strong appeal to audiences and can translate into higher box office earnings.

**Influence of Ratings on Gross Earnings**:
The correlation coefficient between average ratings and gross earnings is approximately 0.21, indicating a weak to moderate positive correlation.
This suggests that while there is some relationship between movie ratings and gross earnings, it is not very strong. Other factors beyond ratings also contribute to a movie's financial success. From our box plot it is important to note as it indicates audiences and critics have a tendency to rate movies within our IQR range but will often score movies below that range as opposed to above it.

**Effect of Release Dates on Gross Earnings**:
There is a statistically significant difference in gross earnings among movies released in different months.
The analysis suggests that release dates have a significant impact on gross earnings, with certain months showing higher revenue generation than others.
Spring and summer months, particularly April to June, appear to be the most profitable for movie releases, but strong revenue is also observed in October and November.

**Implications and Further Analysis**:
Movie studios and filmmakers can use these insights to make strategic decisions regarding genre selection, release timing, and marketing efforts.
While certain genres and release months show higher revenue potential, it's essential to conduct further analysis to understand specific trends and patterns comprehensively.
Factors such as competition, audience demographics, marketing strategies, and the quality of the film itself can also influence box office performance and should be considered in decision-making processes.

In conclusion, while genre selection, ratings, and release timing play significant roles in determining box office success, a holistic approach considering various factors is necessary for maximizing revenue and audience satisfaction in the film industry.

# Recommendations

Based on the conclusions drawn from the analysis, several recommendations can be made for movie studios, filmmakers, and other stakeholders in the film industry:

**Strategic Genre Selection**: Given the popularity and revenue-generating potential of the Adventure, Animation, Action, and Sci-Fi genres, Microsoft should consider investing in projects within these genres. Audience preferences and trends within these genres to ensure alignment with audience expectations.

**Focus on Quality**: While genre selection plays a crucial role, it's essential not to compromise on the quality of the film itself. Investing in compelling storytelling, high production values, talented cast and crew, and innovative filmmaking techniques can enhance the overall appeal of the movie and increase its chances of success, regardless of genre.

**Optimal Release Timing**: Microsoft studios should strategically schedule releases during peak months such as spring and summer, particularly April to June, to capitalize on higher audience turnout and maximize revenue potential. However, they should also consider factors such as competition and audience demographics when planning release dates.

**Marketing and Promotion**: Effective marketing and promotion strategies are essential to generate buzz and create anticipation for movie releases. The studio should invest in comprehensive marketing campaigns across various platforms, including social media, traditional advertising channels, and promotional events, to reach and engage with target audiences effectively.

**Continuous Analysis and Adaptation**: The film industry is dynamic, with audience preferences, market trends, and external factors constantly evolving. Movie studios should continuously monitor industry trends, conduct audience research, and analyze box office performance to adapt their strategies accordingly. Flexibility and agility in responding to changing market dynamics are essential for long-term success.

**Diversification and Innovation**: While certain genres may dominate the box office, there is also room for innovation and diversification. Studios should explore new and emerging genres, experiment with hybrid genres, and support diverse voices and storytelling perspectives to cater to a wide range of audience tastes and preferences. However in this endeavor it is important to note that it is better to support this as independent lower-budget features as a testing ground for audiences.

By implementing these recommendations and staying attuned to industry trends and audience feedback, movie studios and filmmakers can increase their chances of success in the competitive film industry landscape.
