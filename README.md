# Exploratory Data Analysis - FinalProject
Final project for week 4 in Coursera Course: Exploratory Data Analysis


## Goal 

The overall goal of this assignment is to explore the National Emissions Inventory database and see what it say about fine particulate matter pollution in the United states over the 10-year period 1999–2008. You may use any R package you want to support your analysis.

## Data

The data for this assignment are available from the course web site as a single zip file:

https://d396qusza40orc.cloudfront.net/exdata%2Fdata%2FNEI_data.zip

The zip file contains two files:

PM2.5 Emissions Data (summarySCC_PM25.rds): This file contains a data frame with all of the PM2.5 emissions data for 1999, 2002, 2005, and 2008. For each year, the table contains number of tons of PM2.5 emitted from a specific type of source for the entire year. 

   - fips: A five-digit number (represented as a string) indicating the U.S. county
   - SCC: The name of the source as indicated by a digit string (see source code classification table)
   - Pollutant: A string indicating the pollutant
   - Emissions: Amount of PM2.5 emitted, in tons
   - type: The type of source (point, non-point, on-road, or non-road)
   - year: The year of emissions recorded

Source Classification Code Table (Source_Classification_Code.rds): This table provides a mapping from the SCC digit strings in the Emissions table to the actual name of the PM2.5 source. The sources are categorized in a few different ways from more general to more specific and you may choose to explore whatever categories you think are most useful. For example, source “10100101” is known as “Ext Comb /Electric Gen /Anthracite Coal /Pulverized Coal”.

You can read each of the two files using the readRDS() function in R, as long as the files are stored in the working directory.

## Questions

You must address the following questions and tasks in your exploratory analysis. For each question/task you will need to make a single plot. Unless specified, you can use any plotting system in R to make your plot.

  1.  Have total emissions from PM2.5 decreased in the United States from 1999 to 2008? Using the base plotting system, make a plot showing the total PM2.5 emission from all sources for each of the years 1999, 2002, 2005, and 2008.
  2.  Have total emissions from PM2.5 decreased in the Baltimore City, Maryland (fips == "24510") from 1999 to 2008? Use the base plotting system to make a plot answering this question.
  3.  Of the four types of sources indicated by the type (point, nonpoint, onroad, nonroad) variable, which of these four sources have seen decreases in emissions from 1999–2008 for Baltimore City? Which have seen increases in emissions from 1999–2008? Use the ggplot2 plotting system to make a plot answer this question.
  4.  Across the United States, how have emissions from coal combustion-related sources changed from 1999–2008?
  5.  How have emissions from motor vehicle sources changed from 1999–2008 in Baltimore City?
  6.  Compare emissions from motor vehicle sources in Baltimore City with emissions from motor vehicle sources in Los Angeles County, California (fips == "06037"). Which city has seen greater changes over time in motor vehicle emissions?
  
The answers for each of the above questions can be found by examining the graph correpsonding to each question. For example, plot1.png contains the graph to answer Question 1. Additionally, the code used to generate each plot can be found by examining the code corresponding to each graph (plot1.R correpsonds to plot1.png).

## Note: To conserve processing time, the code must be run sequentially. The data set used in this analysis is large. Therefore, the data is imported in the first code (plot1.R). The remaining codes (plot2.R - plot6.R) are constructed to use the data intially imported in plot1.R.
