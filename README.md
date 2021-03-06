# Scraping and parsing MLB xml game files

MLB makes these files available on their website, organized by date, e.g. http://gd2.mlb.com/components/game/mlb/year_2018/month_06/day_08 for all games on June 8, 2018. But to be able to do pitch-level analysis on these, we have to parse through the XML. The notebooks here are what I used to download and parse the XML. The parsing code runs in about 15 minutes for all 4 seasons. Since new elements are added to lists each time through the loops, this slows down as more and more data is accumulated. It could be optimized by creating the dataframes early and appending the accumlated data to them at intervals, but since this is just 4 seasons, and isn't code that needs to be run more than once, I haven't implemented that.

Data, plus some analysis and predictive modeling, can be found on Kaggle: https://www.kaggle.com/pschale/mlb-pitch-data-20152018
