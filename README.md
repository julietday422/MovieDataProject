# MovieDataProject
![RE4OAgf](https://user-images.githubusercontent.com/100893109/164759541-96a1bbd6-8f62-4096-b7c8-53fc5cddc306.jpg)

## General Overview:
The purpose of this analysis is to find trends in movie data that will allow Microsoft to decide what kind of movies to make at their new Microsoft studio. Since Microsoft is just getting into the movie business, they need actionable insights to decide what kind of films to create.

## Business Problem:
As a business, Microsoft's goal is to make money. With so many attributes to a successful movie, Microsoft needs to know what kind of movie to make and how to make it, in order to earn a net profit.

This data will explore that question from three angles:
1. Runtime
2. Time of year the movie is released
3. Production budget

## Data Understanding:
The data used for this analysis came from two sources: The Movie Database (TMDB) and The Numbers (TN).

The TMDB data was used to analyze runtime, with a total of 4,766 data points used after cleaning the data. This data was collected from a dataset on kaggle: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

The TN data was used to analyze the movie's premiere month and production budget, with a total of 5,782 data points. This data was collected from a dataset provided by the Flatiron School.

Both TMDB and TN are reliable data sources that provide movie insight based on a variety of factors.
The main limitation of this data is that it only comes from 2 sources with a total of 10,548 data points. 

![Unknown](https://user-images.githubusercontent.com/100893109/164762066-f3ff2a0b-f51c-4838-a9e3-742396ab575b.jpg)

<img width="307" alt="Screen Shot 2022-04-21 at 2 52 03 PM" src="https://user-images.githubusercontent.com/100893109/164762045-bea6f1f7-d39a-4fb9-bcb0-54e723cd4496.png">

For the TMDB data, used for evaluating runtime, the three columns used were budget, revenue and runtime, and the rest were dropped. There were only 2 null values between these three columns (out of 4,766 data points) so these were dropped. Further, there were 35 data points with values of 0 for runtime, so these were dropped as well, as a runtime of 0 would equate to a null value in this instance. The net profit was then calculated by subtracting the budget from the revenue and this was plotted against the runtime. 

For the TN data, used for evaluating release month and production budget, the data had been pre-cleaned for null values and values of 0. I therefore went ahead and separated the release month from the rest of the date and the budget and revenue values were changed from object types to integers. The net profit was then calculated and the top 100 movies based on net profit were pulled out to be compared to the rest of the data for the premiere month analysis. The two graphs were then plotted. 

## Data Analysis- Runtime:

![Run Time vs  Net Profit](https://user-images.githubusercontent.com/100893109/164948817-bec7c4fb-beda-4167-afbb-e5958c4e4c79.png)

## Results/ Recommendation: 
With a correlation coefficient of 0.225, there is a very weak, positive correlation between the a movie's runtime and the movie's net profit. 
Most movies are between 90-140 minutes, however, the runtime of the movie does not have a strong correlation to the sucess of the movie, so Microsoft can choose to make the movie as long as they want without too much concern.   

## Data Analysis- Release Month: 

![Frequency of Movies Premiered Per Month](https://user-images.githubusercontent.com/100893109/164948888-4915b9f6-6f8e-4756-a4b7-5ce9a0d045de.png)

## Results/ Recommendation: 

A much higher percentage of the top 100 gross movies premeried in May, June, July, November and December, which makes sense given the summer months and before the holidays are popular months to go out.
The movies not in the top 100 are much more evenly distributed throughout the year.
My recommendation would be to premiere your movies over the summer or before the holidays in order to have a larger audience.

## Data Analysis- Production Budget:

![Production Budget vs  Net Profit](https://user-images.githubusercontent.com/100893109/164948917-e2c94966-bf8d-4822-951b-7db892c07b25.png)

## Results/ Recommendation: 
With a correlation coefficient of 0.608, there is a moderately positive correlation between the production budget and the movie's net profit, however this is not an absolute. Once the production budget gets above 50m, the chances of making a higher net profit increases, as we can see from the best fit line.

## Conclusion:

Runtime: Most movies are between 90-140 minutes, however, because the runtime of the movie does not have a strong correlation to the sucess of the movie, Microsoft can choose to make the movie as long as they want without too much concern.   

Premiere date: A much higher percentage of the top 100 gross movies premeried in May, June, July, November and December, compared to the rest of the movies which premiered in a more even distribution throughout the year. Therefore, Microsoft should premiere their movies over the summer or before the holidays. 

Production budget: There is a positive correlation between the production budget and the movie's net profit, however this is not an absolute. Once the production budget gets above 50m, the chances of making a higher net profit increases, as we can see from the best fit line. 

## Next Steps:

To further analysis how the production budget relates to net profit, it would be helpful to break the production budgets into bins (0-10M, 10-25M, 25-50M, etc) and calculate the mean of each budget as it relates to the mean net profit. 

Another helpful factor to analyze would be which genres of movies that have the highest net profit. 

Lastly, as discussed above, ancillary revenue has a big impact on net profit so analyzing the ancillary revenue of movies would be another helpful data point for Microsoft. 

## For Additional Information

Project Workbook: https://github.com/julietday422/MovieDataProject/blob/main/ReportNotebook.ipynb

Presentation: https://github.com/julietday422/MovieDataProject/blob/main/presentation.pdf

Images (JPEG and PNG): https://github.com/julietday422/MovieDataProject/tree/main/Images

For any additional questions, please contact Juliet Day at julietday422@gmail.com

## Repository Structure

├── README.md                           <- The top-level README for reviewers of this project
├── ReportNotebook.ipynb                <- Narrative documentation of analysis in Jupyter notebook
├── Movie Analysis Data.pdf             <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
