### An Initial Analysis/Prediction for the Production Awards Program at the New York Film Festival ###


**Abstract**

In this project, we used data scraped from the Box Office website, Box Office Mojo, to build a model that showed correlations between the success of documentaries and various components of distribution channels. We used the listing that ranks Documentary genre films by Box Office numbers and used the international gross as our target value. The pitch was tailored towards the New York Film Festival (NYFF)’s Production Awards section and their new focus on documentary filmmaking. As the funders of seed production money during the development of the film’s production & distribution strategies, NYFF also advises filmmakers and connects them to their network. So they wanted to see what features correlate highly with the success of viewership for the film as measured by overall (international) gross at the box office. 


**Design**

With the above question shaping this project, we set out to look at the features that affect the box office after the production of the movie (the production side is largely shaped by artistic insight and freedom so we wanted to first look at the distribution features; our suggestions are below for what features we would like to model in the future on the production side). The distribution features we chose to model were the max number of theaters that the film was shown in as well as the number at the opening, and the choice of distributor for the film. As we readily had access to the data, we also looked for any correlations between runtime and release year and our chosen target: international gross. We chose to ignore the features domestic gross or gross at opening as these are highly collinear with the international gross (since a majority of measured viewership happens in the US which is where the most industrialized film industry is located). 

We suggest at the end of our project for NYFF to commission us for another project in which we model features on the production side. The features we would like to collect data on on this side would be: Budget (not readily available on the Box Office Box, most probably because documentary filmmaking is rather an independent process). 


**Data**

*Box Office Mojo* 
- We scraped all the movies on the documentary listing on the Box Office Mojo website, observations amounting to 1969 movies. Removing outliers we worked with 1571 movies for our model. 
- Initial feature included the link stub for the film’s individual page and between this table and the data from the films individual page the features scraped include: rank, title, lifetime gross, maximum number of theaters shown in, opening gross, theaters shown in at opening, release date, distributor, domestic gross, worldwide gross, budget, runtime, MPAA and genres. 
- We then scraped the credits pages of each movie to get the features: director, writers, producers. 

*Wikipedia*
- Using the data we got from our Box Office Mojo scraping, we constructed a column listing the Wikipedia URL for the director. 
We then scraped Wikipedia in order to collect information on Birthplace, Birthday (year/age would be important here) and Country of Origin of the Director. 
- Also 1969 observations.
- For the ‘further part’/ 2nd commission from the NYFF mentioned above, this information would be used to look at correlations between features on the production side of filmmaking and box office gross. 


**Algorithms**

*Web Scraping* 
- The data was collected from the 2 websites and then parsed with BeautifulSoup. 

*Linear Regression* 
- The model was built after a CV comparing the Simple, Ridge and Polynomial linear models. The R2 scores we got for the Simple & Ridge models were almost identical, and we chose to continue with Simple regression. 
- We adjusted our target by taking its logarithm. 
- We did feature engineering to test whether polynomials of certain features would help but in the end we did not find that our model performed much better. Starting out our  R2 score was 0.21 and even though we were able to improve it to 0.29; in the end our test scores were 0.097 and we never got a working linear model resulting in us being able to conclude that the correlation between these features and our target is rather nonexistent.  
 
*Visualization*
- We did do diagnostic plots as well as visualizing the relationships between each feature and the target in order to try and understand the lack of correlation. 


**Tools**
 - BeautifulSoup for web scraping
- Python/ Pandas for initial EDA and then building the regression models  


**Communication**

We presented our findings to the NYFF Production Awards Team with our conclusions and asked them if they would like to continue their modeling on the features affecting the production side. This would involve looking at features such as budget and crew member’s locations. If the models would find that there are correlations on that side, the NYFF Production Team could advise their grantees to keep these features in mind in building their cast/crew. 
