# connect-to-census

In this assignment, you will connect your data to census data and do a bit of basic exploratory data analysis (EDA) on your dataset. The EDA will be in 1-D (distribution of your data) and 2-D (comparing your data to census variables).

## Assignment

Identify the geospatial columns in your data. You may have addresses or latitude and longitude. In this assignment you will 

1. In the `connect-to-census.ipynb` notebook, add code to:

    a. download your data
    b. convert addresses --> lat/long (if the data doesn't already have lat/long)
    c. convert lat/long to census geography codes (like 'GEOID', 'STATE', 'COUNTY', 'TRACT', 'BLOCK', etc...). you may want to have more than one level of geography so you can do the analysis at different levels later on.
    d. this notebook should output a file containing your data and the census geographies you're interested in.

    Example notebooks to help you with all this will live in [this repository](https://github.com/data4news/census-examples). You may use R or Python (or a combination of the two).


2. In `merge-with-census.ipynb` notebook, download some census data using `tidycensus` and merge it with your data.

3. In the `1d-eda.ipynb` notebook, do some basic exploratory data analysis on your data in one dimension. Here you will explore the **distributions** of your data (histograms, boxplots, dotplots, etc).

4. In the `2d-eda.ipynb` notebook, do some basic exploratory data analysis on your data, but this time, merge in some census variables you're interested in. 


## Usage

1. Rename `.env.example` to `.env` and put in your census API key. 
   
    _(FYI there is a file in this repo called `.gitignore` that will prevent `.env` from being tracked by git so you don't push your census key on accident._

2. Run the notebooks.

## Note about large files

If your data is too big (bigger than ~50MB), just upload the code to transform your data, not the data itself. If you want to make sure to never upload the datafile to git, just add the name of the file to the `.gitignore` file.