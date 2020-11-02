# Exploring health searches
- A Python pandas data exploration assignment for class 5007.

## Instructions
- If running into seaborn errors, run `pip install seaborn` 

___
## Observations
___
### Descsriptive Statistics
**Fig. 1** Offers a data distribution overview, that is more detailed in figures 1.1-1.9.
- Data distributions vary per search topic, as well as per year within a single search topic. 
    - Cancer standard deviations fluctuate between 6 and 7 
    - Cardiovascular 
        - The mean tends to be pretty close to the standard deviation, suggesting a ~relatively normal distribution
        - Standard deviation had a spike in 2005 (at around 14.3), to around twice as much as that in 2004. It then wavers in the following years, at standard deviations 9 and higher. 
        - Data distribution suggests the least searches were in the year 2004, suggesting that search interest in this area is increasing (as evident by the starting median, a resistant metric, of 6 in the year 2004, and the median of 34 in the year 2017)
    - Stroke



    - ~Overall search topics across the years depicted here exhibit sharp density curves with relatively long tails, suggesting more reliable/less anomalous data

### ~Fig. 2 diagrams
In studying the correlation heatmaps in figure 2 (fig. 2.1 - 2.9), the following could be observed:
- Correlations increase with time. That is there is a stronger positive correlation between for instance 2011 cancer searches and 2012 cancer searches, suggesting that serach results have spiked since 2011 (where correlations with subseueqnt years are with the stretngth of at least r = 0.7)

### Fig. 3 & 4 diagrams
Given the size of the dataset (127 rows and cols in correlation matrix), the data has been broken down for ~exploration by year.
- The highest intra-year correlation is that found in year 2005, **Fig.3.2**, between depression and diabetes searches. 
- Zooming in on the scatter plot for the year 2005, in **Fig. 4**, a strong positive correlation can be seen, where an increase in depression searches in 2005 are strongly correlated with an increase in searches in diabetes in the same year. 
    - There's a heavy clustering towards the lower left quadrant of the scatterplot, where data distribution is most dense, offering a higher confidence in each variable's predictability of the other.
    - The 2005 searches exhibit some anomalies, most noteworthy being that at 100 depression sarches, for which the frequency is mirrored in diabetes searches. 
      
