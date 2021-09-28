### Analysis of Documentary Film Success in Film Industry

Scraping the BoxOffice Mojo website for data on documentary films, the project aims to find out what features are relevant
in determining the success of a documentary film (measured by international gross boxoffice number). The numeric features 
obtained so far are plotted in the following heatmap and pairplot. The numeric features that will be regressed include: 
Max number of theaters the film showed at (max_theaters), its boxoffice opening week(opening), the number of the theaters it played at
the opening week(open_th), budget, runtime, and the year it was released. Looking at the heatmap and the pairplot, the 2 features 
that might be used for regression include max_theaters & budget (although this one contains too many null values). 

![Heatmap](https://github.com/zey-o/Lin_Reg/blob/main/Lin_reg_heatmap.png)
![Pairplot](https://github.com/zey-o/Lin_Reg/blob/main/Lin_reg_pairplot.png)

Further features include: rank, title, distributor, domestic total gross, worldwide gross, MPAA, Genres, 
Director, Writers, Producers that scraped from the BoxOffice Mojo website as well as director's birth place, birthday 
scraped from the Wikipedia website. 

Regression will continue by creating dummies from the genres and distributor features and (time permitting) the country of origin of 
director (the nonnull values on this feature is about 15-20% of the data, so might not be usable). 
