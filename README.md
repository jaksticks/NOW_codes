# NOW_codes

Data and Jupyter notebooks for the paper "Do species factories exist? Detecting exceptional patterns of evolution in the mammalian fossil record".

We have run the experiment with two different spatial resolutions, one using a 100 km and on a 500 km radius around a given geographic focal point. The data and notebooks are in folders radius100 and radius500, respectively. Both folders consist of five sub-folders: csv, figures, geopandas, notebooks and NOW_rawdata. 

The folder csv contains a number of csv-files that were generated as part of the analysis. The folder figures contains all the figures generated. The folder geopandas contains a number of files used to create geographic maps. The folder notebooks contain all the Jupyter notebooks that essentially form the whole data processing and analysis pipeline. The folder NOW_rawdata contains the original fossil occurrence data downloaded on 26.4.2020.

The Jupyter notebooks found in the notebooks folder are in numerical order such that running them in order recreates all of our results. It is also possible to run each notebook in isolation.

## Short description of notebooks

1. createDataFrame is used to create a pandas Dataframe from the original data txt-file.

2. cleanDataFrame is used for pre-processing and cleaning the data.

3. occurrences is used to determine for each species in which time units they occur and when they occur for the first and last time.

4a. localityFeatures is used for gathering useful information regarding each unique location in the data set. 4b. gridFeatures is used to create a dataframe that will be used later for gathering information related to each spatial grid point.

5a. localityOccurrences is used for calculating weighted occurrences for each locality in the data set. This is done for the designated time unit of the locality and for one time unit before and after the designated time unit. 5b. gridOccurrences does the same, but for each spatial grid point (instead of fossil localities).

6a. regressionAndExpectations is used for performing a logistic regression to find out how many first and last occurrences we should expect in a given locality based on the number of occurrences in the preceding and following time units within the focal area of the locality. 6b. migration does a similar analysis to estimate expectations for first and last occurrences locally for any given spatial area.

7. significance is used to estimate how significant is the difference between the numbers for actual and expected observations.

8. mapSignificance is used for making various visualisations of the results, particularly heat maps of spatial patterns.

9a. analysis is used to carry out a number of analyses and visualizations of the results. 9b. species_geodesic_areas is used to carry out further analyses of the results, in particular to calculate ages and spatial ranges of species that originated in different hotspots (and non-hotspots).


