# Movie Data Analysis Project
Table of Content
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Results and Findings](#results-and-findings)
- [Challenges in Analysis](#challenges-in-analysis)

### Project Overview
The main goal of this data analysis project is to provide insights into the performance and trends of movies produced during the period of 2012 to 2016 
I looked at various parts of movie data to find patterns and changes in the industry, and to provide recommendations based on the results of the analysis 

### Data Sources 
Movie Data: The primary dataset used for this analysis is the "Movie Data Source File.xmls" which contains detailed information about each movie's performance, directors, cast etc.

[Movie Data Source File.xlsx](https://github.com/user-attachments/files/16419911/Movie.Data.Source.File.xlsx)


### Tools 
 - Power Query - I used Power Query for Data Cleaning
 - Excel, Pivot Tables - These were used for my Data Analysis, Creating Reports and Visualizations

### Data Cleaning and Preparation Process 
The following tasks have been performed during the initial data preparation step:
 - Data Loading and Inspection
 - Discovering and Eliminating Errors and Missing Values
 - Data Cleaning and Formatting
The Excel file after the data cleaning & preparation process completed can be found here
[AANPLdFKQ5qgmO5lWys6_Movies Data Ready for Dashboard file.xlsx](https://github.com/user-attachments/files/16419986/AANPLdFKQ5qgmO5lWys6_Movies.Data.Ready.for.Dashboard.file.xlsx)


   ### Exploratory Data Analysis
 - Which genres were the most financially successful during these years?
 - Which actors achieved more success and generated more revenue?...

  ### Results and Findings
   Examples:
   - The most profitable movie was "The Devil Inside" which had the budget of only USD 1 mln, but it brought the Box Office Revenue of USD 101.8 mln
     
   ![Best Profitable Movie](https://github.com/user-attachments/assets/6a5d45a4-fcc3-44b3-8386-775353910738)

   - The least profitable movie was identified as "The Oogieloves in the Big Balloon Adventure" for all years checked with the worst ROI
   - Top 5 movie revenue generating movie genres and top 5 actors in those movies
   - The best Director of the most successful movie in these 5 years
   - The most profitable season for releasing movies
     
![Movies data Dashboard](https://github.com/user-attachments/assets/1ebd7987-70b9-40ad-968b-6ff26fc0bb0f)


  ### Challenges in Analysis 
  #### M Language 
  One of the challenges I encountered during my work was a specific code for Grouping in M Language in order to combine two genres together for further analysis. 
  Initially there were 2 separate columns for 2 genres a movie was categorized. It was necessary to combine both genres into one showing a combination of genres with / in a 
  certain wording order only such as action/comedy, but not comedy/action etc. 

  ``` = Table.Group(#"Sorted Rows1", {"Movie Title"}, 

                                            {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text}, {"AllData", each _, type table [Movie Title=nullable text, Release Date=nullable date}
  ```

  
   
   
