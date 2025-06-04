# 🗺️Plotting GDP Data on a World Map - Part 1

In this project, you will build world map visualizations of GDP data using Pygal, similar to those on the World Bank website. The main goals are to practice using multiple dictionaries, clean and unify datasets, and explore Pygal’s features by referencing its documentation. This project emphasizes real-world data handling and visualization skills.

------

# Project description
The project consists of multiple problems. Each problem will utilize functions you wrote for the previous problems. You can also download all of the files used when testing your code as a zip file.

### Problem 1: Create a dictionary that maps Pygal country codes to World Bank country names
The main task of this project is to process the World Bank GDP data and build a dictionary whose values represented the GDP data for a given year that can be plotted with Pygal.  The key step in this process is reconciling Pygal country codes/names with the World Bank country names. So, you first must write a function called reconcile_countries_by_name which takes plot_countries, a dictionary mapping country codes used by a plot library (such as Pygal) to the corresponding country name, and gdp_countries, a dictionary whose keys are the country names used within the GDP data.  The values in the gdp_countries dictionary are irrelevant for this function, but presumably contain GDP data for each country. The reconcile_countries_by_name function should return a dictionary and a set.  The dictionary should map the country codes from plot_countries to country names that match between plot_countries and gdp_countries. It should not contain key-value pairs for the countries within plot_countries that do not appear in gdp_countries.  The set should contain all of the country codes within plot_countries that did not match any countries in gdp_countries, so is effectively the set of countries that the plot library knows about but cannot be found within the GDP data.

### Problem 2: Transform GDP data for given year into a form suitable for a world map plot
Your next task is to implement the main function that processes GDP data. You must write a function called build_map_dict_by_name which takes gdpinfo, a GDP information dictionary (as used in the first project), plot_countries, a dictionary mapping country codes used by a plot library (such as Pygal) to the corresponding country name, and year, the year for which to create a GDP map dictionary, expressed as a string. The build_map_dict_by_name function should return a dictionary and two sets.  The dictionary should map the country codes from plot_countries to the log (base 10) of the GDP for the associated country in the given year. (The logarithmic scaling is chosen to yield a better distribution of color shades in the final plot.) The first set should contain the country codes from plot_countries that were not found in the GDP data file.  The second set contains the country codes from plot_countries that were found in the GDP data file, but have no GDP information for the specified year.

### Problem 3: Create an SVG image of the GDP data plotted on the world map
As the final part of this project, your task is to write a function that takes the GDP map information computed using build_map_dict_by_name and create a world map plot using Pygal. You should write a function called render_world_map which takes gdpinfo, a GDP information dictionary, plot_countries, a dictionary mapping country codes used by Pygal to the corresponding country name, and year, the string year for which to create a GDP map dictionary, and map_file, the string name of the file to write the output plot to.

Using these inputs, you should use Pygal to plot the logarithmically-scaled GDP data on a world map. Review Pygal's documentation on world maps for more details. Make sure that you plot not only the GDP data, but also the countries which are missing from the GDP data entirely and the countries that are contained within the GDP data, but have no data for the given year.

The output plot should be stored in an SVG file with the name specified by the map_file.


# Key features

1. Match Pygal country codes with World Bank country names.
2. Convert GDP data to log-scaled values for a specific year.
3. Identify missing or incomplete GDP data.
4. Plot the GDP data on a world map using Pygal.
5. Export the visualization as an SVG file.


---------



