This project is an analysis of 2 datasets from kaggle.com. One is video games ranked by sales, and the other is video games review scores from critics and user reviews.

Data Merging File:
In order to merge these two datasets to analyze them efficiently, I tried to match by name all video games that appeared in both datasets.

!Disclaimer, I am not using the most accurate verion possible of cleaned data. 
Due to the datasets containing sequels and other iterations of games in the series
I could not easily get clean results without warranting the need for hours of manual checking for an additional 4000 additional entries
As a result, my cleaned data includes only the 7800 game titles that had an exact name match between both datasets
If you want the most accurate results possible, you will need to manually check any name matching you do for sequel, prequel, or version changes when trying to match names

Once I matched the names of the game titles that exist in both sets, I merged the sets together by name(game title), platform, and year(release year), however some changes needed to be made
  First off, in the video games review dataset, the release date column is the specific date the game released whereas the column in the video game sales column is just by year. 
  To fix this I simply converted the release date column in the video games review dataset to just be by year.

  Secondly, the platform names in both datasets vary, so to fix this, I made a road map to convert all the platform names to a unified naming style to avoid repeats or confusion

After cleaning the rows, I merged the two datasets by name, platform, and year as mentioned above and exported a brand new CSV file that contains the dataset I will analyze.

Analysis File:
For this analysis, I will create 2 sets of scatter plots. For each set of scatter plots, they are a comparison of number of sales by region and then by global sales, and comparing them
to either critic scores or user review scores.

Sales are in represented in millions, critic scores are out of 100, and user reviews are on a scale of 1-10.

After running the code, you can see that the scatter plots show some slight correlation between sales and critics scores with some games that got higher scores having more sales. However, 
there is still nothing all that strong suggesting that the critic reviews changed that outcome. Some games seemingly stand out in sales in the Japanese market with some games seeing a 
larger number of sales as critics scores go up. Though it should be noted that the Japanese market is significantly smaller than that of North America and Europe as represented by the scale
of the sales axis only going up to 7 million at the highest where North America and Europe have outliers significantly above 25 million sales.

You can also see a similar pattern in the scatter plots representing sales compared to user scores. There are a number of outliers especially for games that recieved higher user scores
though still the main body of the scatter plot doesn't suggest any strong correlation to user scores and sales. 

Overall, the analysis seems to show that neither critic nor user review scores seriously affected the number of sales for any of the games in the dataset if at all. For any outliers in the
charts, it is likely that those games recieved either local or global popularity due to the expected quality, hype, marketing, or any other related reason. It should be noted though that
the outliers in all the plots generally encompassed a high number of sales and a higher review score on average, which rightfully suggests that games with higher sales are likely more
associated with better scores. 
