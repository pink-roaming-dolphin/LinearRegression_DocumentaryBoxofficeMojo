**Sundance Film Festival & Box Office** 

For this project, I will be looking at the films that were nominated in any category at the Sundance Film Festival over the last 20 years. I’ll collect information about the movies to then see if there are certain features that would make an independent movie have more of a chance of success (measured by reach, measured by Box Office numbers).  

I will look at the Sundance Film Festival Event History on the IMDB website and scrape this page to get a list of all those nominated films over (approximately) the last 20 years (scrape to get the website link for each movie). Then having this list handy, I would go to the website of each movie to scrape the information for that movie. Features would include IMDB Rating, Popularity, Runtime, Year, Director, Writers, Stars, Genres, Release Date, Country of Origin, Languages, Filming Locations, Production Companies, Box Office Details (Gross US & Canada, Gross Woldwide, Opening weekend US & Canada), Runtime. Each observation will be a movie and my target value is going to be the box office revenue. Once all the data is scraped, using linear regression models I want to look at the relationship between the Gross Box Office Worldwide and each of these features. I also want to see if there are certain genres of independent film that are more susceptible to gaining more mainstream recognition (ie. Academy Awards: The method here would be to scrape the events listing for Academy Awards to see if a movie has been awarded any Academy Awards in the corresponding year) as well as seeing if production budget is a factor (the- numbers.com seems to have a fairly wide ranging budget approximation but have to see if this is comprehensive enough). Lastly, I would like to scrape data about the Directors from Wikipedia, and find out about correlations between their Date and Place of Birth, and Education (here I’m curious about diversity in the movies and the relationship to success: the Date + Place of Birth & Education are the consistent features on the Wikipedia page, would like to access Gender, Race also if possible but have to dig around for this). 

The MVP would be a series of plots using the linear regression modeling (most probably from SKLearn) and showing the correlation over the years between the ‘viewership rate’ as measured by Box Office numbers (target value) and the production budget of an independent movie, the background of the director (might have to be limited to date & place of birth and education). 
