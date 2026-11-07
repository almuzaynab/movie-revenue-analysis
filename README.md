# movie-revenue-analysis
Using Python (NumPy, Pandas, and Seahorn) on Jupyter Notebook, exploring and cleaning IMDb movie data to determine which metrics and measures directly impact gross movie revenue.  

---

Technical Skills: 

Python ( Pandas, Seahorn, Matplotlib.pyplot libaries) on Jupyter Notebook

---

Methodology: 

Importing all of the necessary libraries and taking an initial look at the data being reviewed. The data being pulled is a movie library with data pulled from IMDb (Internet Movie Database)

<img width="1450" height="567" alt="image" src="https://github.com/user-attachments/assets/84a0dade-a856-4b97-8a0a-4677bcb2aaa7" />

<img width="227" height="346" alt="image" src="https://github.com/user-attachments/assets/83e9b090-717d-416e-917e-be95dbf29b8e" />

After reviewing the data and understanding the data being worked with, begin data cleaning. Involves checking for nulls, removing nulls, and removing duplicate values. 

---

Now that the data is cleaned, we want to begin looking at the reviewing the movies with a higher revenue. Sort the dataframe from highest to lowest grossing movies. 

<img width="1376" height="372" alt="image" src="https://github.com/user-attachments/assets/b3f96a6f-9361-408e-bee9-f47c1a5d2428" />

We can begin to explore different correlations to see what best impacts the gross income. A popular concept is that a movie's budget is directly correlated to the gross revenue. We can explore this by using a scatter plot. 

<img width="1003" height="705" alt="image" src="https://github.com/user-attachments/assets/40723166-fb9b-4bdd-a600-bec826de8827" />

This shows a positive correlation line between a movie's budget compared to the gross revenue of the film. Though this graph confirms a positive correlation, we could also verify this by pulling correlation values. 

<img width="710" height="272" alt="image" src="https://github.com/user-attachments/assets/198fd515-cd24-4e86-aee8-743722a3d7c8" />

<img width="919" height="706" alt="image" src="https://github.com/user-attachments/assets/7f303681-7745-40b3-9940-828dcda2ce99" />

This validates the hypothesis that the budget of the movie has the highest correlation to the gross revenue. The matrix above was only able to pull for metrics in the initial cvs file that were numerical values. This limits the option to look at correlations for non-numerical metrics. For simple calculation, let's associate the non-numerical values with a paired numeric value.

<img width="1260" height="372" alt="image" src="https://github.com/user-attachments/assets/86135401-ba25-44a4-be11-578f32cd08db" />

Make the correlation table and a correlation matrix based off of df_numerized as opposed to df to capture more metrics. 

<img width="1385" height="612" alt="image" src="https://github.com/user-attachments/assets/6f9abfba-4d40-4405-8ea6-286dd026ea3d" />

<img width="983" height="757" alt="image" src="https://github.com/user-attachments/assets/8da8aeab-c3a9-45f0-8210-aa0d67bf7ff2" />

As we expanded the amount of metrics compared, the table and matrix are slightly cluttered. However, due to the nature of the coloring in the matrix, it is easier to identify higher correlated points. Looking at the tiles that are more orange, we can see that a good correlation stems from the movie's budget or the votes. What votes represent on IMDb are the number of user votes on a movie. Which makes sense, the more people see a movie, the more people are going to vote on it. Another way this can be interpreted, the movie has more marketing to get people to see movie and as a movie gains popularity, more people are likely to go out to see the movie. 

--- 
Conclusion and General Notes: 
- Budget and Gross Revenue are highly correlated. The larger the budget, the more people are intrigued to see a movie.
- Expected factors like genre or company was found to have very little correlation to a movie's gross revenue. Although, it is to note that larger companies can put larger budgets for a movie. 
