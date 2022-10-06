# Surfs Up

## Overview

A former professional surfer is considering investing in a hybrid surf and ice cream shop on the island of Oahu. The investor is concerned because a previous venture failed, largly due to weather. The investor is enthusiastic about this idea but would like further information about weather in the area, in particular for the months of June and December before signing off on the project.

## Results

### Methods and Tools
1.  Data was provided as a SQLite database comprising historical weather observations in Hawaii in addition to data specific to individual weather stations.

2. Python was used for the analysis with the addition of:
- SQLalchemy to communicate with the database.
- Pandas to create DataFrames and generate summary statistics.
- matplotlib to generate figures.

### June and December Observed Temperatures

!['June'](/assets/june_temp_summary.png)

!['December'](/assets/december_temp_summary.png)

The summary statistics for all observed temperature measurements from the months of June and December are shown above.

Differences between these months include:

- The mean temperature in June is, roughly, 4 degrees F higher than December's mean.

- June's median temperature is 4 degrees higher than December's median temperature.

- June's maximum temperature is only 2 degrees larger than December's, however, June's low is 8 degrees higher.

A visual representation of the these differences is shown below:

!['Box_Plot'](/assets/comp_plot.png)

## Summary

Despite the differences highlighted above, the weather appears similar in both months. To get a better picture of the conditions it would be useful to determine additional factors. One potential question is which of the weather stations is relevant to our business venture? Given that Oahu has been selected as the island we will be located on and that the primary investor could be considered a surfing expert in regard to both weather and approriate beach conditions, there may aleady be a more specific location on Oahu that our investor has in mind. If this is the case it may alter the dataset if only stations located sufficiently close to the chosen location are selected when retrieving data. This may also include eliminating stations located at higher altitudes since we are primarily interested in sea level conditions.

If there is a 'prime' temperature for surfing and enjoying ice cream, a filter should be applied to only select from that range. This would allow a count and average of the number of days that normally fall within this range for each of the months.

Instead of looking at the month overall, the individual days could be extracted from the dataset. This could provide a more granular insight on trends thoughout the month. For example, is there a day December after which it is often too cold to surf?

The database provided contains a wealth of information, however, it lacks oceanographic and wind information that may be important additions to temperature and precipitation data. The investor would be well served to encourage the selection, cleaning, and merging of a dataset with this information.