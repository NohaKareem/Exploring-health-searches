# Exploring health searches
- A Python pandas data exploration assignment for class 5007, using [kaggle data](https://www.kaggle.com/GoogleNewsLab/health-searches-us-county).

## Instructions
- If running into seaborn errors, run `pip install seaborn` 
___
## Observations
___
### Descsriptive Statistics

- The dataset samples health related seasrches in 9 different topics/keywords, across 210 US metropolitan areas, across 14 years (producing 126 search-frequency columns, in addition to two geographical columns).

- **Fig. 1** Offers a data distribution overview, that is more detailed in figures 1.1-1.9.
    - Data distributions vary per search topic, as well as per year within a single search topic. Below focuses exploration in the cardiovascular-related searches.
        - Exploring cardiovascular-related searches' descriptive statistics
            - The mean tends to be pretty close, throughout the years, to the median, suggesting a relatively normal distribution. This is illustrated by the histograms in fig. 1.2, where the central tendency metrics tend to cluster around the dataset's center, with some exceptions, such as in 2004 and 2005 where a more obvious skewing occurs towards the right. Such skewing is being mirrored in a more pronounced discrepancy between the mean and median. For instance, 2005 hosts a median of 15, and a mean of around 18.67 accounting to the right skewing given its sensitive, non resistant nature.
            - Standard deviation had a spike in 2005 (at around 14.3), to around twice as much as that in 2004. It then wavers in the following years, at standard deviations 9 and higher. The spike suggests a higher variation between metropolitan areas where some would be searching more than others. Lower standard deviations would attribute to more relatable search frequencies across different regions, suggesting a topic of higher nation-wide interest.
            - Data distribution suggests the least searches were in the year 2004, suggesting that search interest in this area is overall increasing (as evident by the starting median, a resistant metric, of 6 in the year 2004, and the median of 34 in the year 2017)
            - Overall search density increase in the year 2017 compared to 2004 is further evident in **Fig. 2.2** depicting boxplots for cardiovascular-related searches in the years 2004-2017. The boxplots' interquartile ranges fluctuate, with occaisonal dips, as in the year 2008, and 2017 (compared to that in 2016, or 2015), but overall exhibits an increase from the starting search frequency seen in 2004. 
                - Looking into the boxplots numerically, in the Cardiovascular search quartiles printed in succession to the boxplots in Fig. 2 plots, it could be seen clearly that the 75th percentile of cardiovascular searches started at a mere 9 searches in 2004, and increased to 41 in 2017 (with an all time high of 53 in 2015).

        - Exploring some observations in stroke-related searches' descriptive statistics
            - The histogras for stroke overall follow a relatively normal distribution, mostly packed around the central tendency, with some skewing towards both ends of graph, indicating that interest tends to spike in a number of cities. 
            - In zooming in on the year 2013, it could be noted that there are two spikes in search interest, namely those around 60 searches, as well as somewhere between 60-80 searches. On filtering the data to those having 60 searches, it could be seen, as evident by the data's shape property, that 12 areas have exhibited such search spike (displayed in table 1.3.1).   

    - As seen in Fig. 1, much of the search topics across the years depicted here exhibit sharp density curves with relatively long tails, suggesting less anomalous data. 

- **Fig. 2** depicts search data distributions' boxplots, categorized by search topic. Overall, the data showcases an overal trend in search increase for all topics in general. 
    - There are some interesting data points, sich as in cancer search where in 2007, that is the only year in given data where there was a point that no cancer-related search was held (minimum of zero). That minimum of zero is a regular occurence however with cardiovascular search, from 2006 and onwards, and occurs in all other datasets at throughout all the years. 
    - As earlier mentioned, there seems to be a staedy increase in search in all fields illustrated, given the overall increasing pattern (with some dips in some search topics) of each topic's interquartile range. 
        - A noteworthy spike in search interest occured in 2011 in depression related searches~

### ~Fig. 3 diagrams
In studying the correlation heatmaps in figure 3 (fig. 3.1 - 3.9), the following could be observed:
- Correlations increase with time. That is there is a stronger positive correlation between for instance 2011 cancer searches and 2012 cancer searches, suggesting that serach results have spiked since 2011 (where correlations with subseueqnt years are with the stretngth of at least r = 0.7)

### Fig. 4 & 5 diagrams
Given the size of the dataset (127 rows and cols in correlation matrix), the data has been broken down for ~exploration by year.
- The highest intra-year correlation is that found in year 2005, **Fig.4.2**, between depression and diabetes searches. 
- Zooming in on the scatter plot for the year 2005, in **Fig. 5**, a strong **positive correlation** can be seen, where an increase in depression searches in 2005 is strongly correlated with an increase in searches in diabetes in the same year. 
    - There's a heavy clustering towards the lower left quadrant of the scatterplot, where data distribution is most dense, offering a higher confidence in each variable's predictability of the other.
    - The distribution could fits to a linear model fairly well with few anomaly points (such as 100,100 or 0,0 at both variables)
    - The 2005 searches exhibit some anomalies, most noteworthy being that at 100 depression sarches, for which the frequency is mirrored in diabetes searches.
    - The data's density, as well as closely packed clustered nature, suggests that there is a relationship worth exploring between depression and diabetes, or perhaps a response to a trend, such as a suggested relationship metnioned in the media, in the year 2005, given how the correlation tapered since. The lower left cluster suggests that the searches were not too dense throughout the year, but when they were present, it was highly predictable that one would occur, given the other, a 76% likelihood that is (correlation coefficient, r, of 0.76).
    - Given the correlation coefficient (r) value of 0.76, the coefficient of determination (r squared) is 0.5776. That is, the correlation accounts for around 57.8% of the data sampled (in searches in question, in 2005). This covers a little over half the data population, suggesting a good enough, albeit not too highly accurate, of a predictive model.  
      
### Fig. 6 diagrams 
The lowest correlation observed was that between cardiovascular and vaccine searches in the year 2017. **Fig. 6.1** plots the correlation scatter plot matrix for the year 2017.   
    - In plotting the cardiovascular and vaccine searches' corerlation in 2017, in **Fig. 6.2**, a flat trend line emerges, affirming a strong **lack of predictability** of either variable to the other. 
    - The scatter plot's density accumulates towards the right half of the graph, around the lower/middle vertical axis (of cardiovascular searches in the year), showcasing more ~vaccine searches than cardiovascular ones in that year. 
    - The data in both **Fig. 6.2** and **Fig. 6.3** has quite a significant amount of data variance, suggesting a non-linear relationship, and thus weakining the reliability of a predictable coefficient-based model. Fig. 6.3  offers a higher rate of predictability than in Fig. 6.2 however (0.27) where the best fit line is skewed upwards, suggesting a positive (albeit weak) correlation where increase in rehab searches tends to coincide withincreased cancer searches (with the exception of the highest cancer searches coincinding with ~half the rehab searches). ~

### Fig. 7 
**Fig. 7.1** examines correlation scatterplot matrix, for the year 2005. 
    - **Fig. 7.2** showcases a negative correlation, of -0.21, where - as depicted by the trend line - an increase in the rehab seaches tends to coincide (albeit not strongly) with a decrease in diarrhea searches. 
        - The predictability of this correlation is rather weak, as evident by the correlation coeeficient.
        - The variability of the data distribution, as demonstrated by this scatter plot, is rather high, thereby reducing the effectivness of the correlation, given the distribution's reduced linearity.
        - The data variance also introduces a number of outliers that affect the overall predictability of the model depicted by the correlation. 
    - **Fig. 7.3** exhibits a case of very weak neative correlation, -0.021, between cancer and depression searches. The plot reveals a straight horizontal line solidifying the variable's lack of predictability for one another, given how any number of cancer searches coincides with relatively the same range of depression searches (with exception to an outlier of 100 depression ~searches given around 45 cancer ~searches). The dataset suggests cancer as an active search topic, given the high density around ~40-80, whie depression having a relatively low search density~ in that given year. 
