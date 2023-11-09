# UFC Power BI Report



## **Ultimate Fighting Championship Power BI Report**

![](UFCMainImage.jpg)
---
**Document Author**                                                   
|Date |Author|Version|Role|                   
|:----|:-----|:------------|:----|                                        
|Nov/08/2023|Fatjan Paloja| 1.0| Power BI Consultant 
## Introduction
![](Ikigai.png)

A few years ago I was notified of the IKIGAI concept of people in Okinava and as a follower of the philosophy "absorb what is useful, reject what is useless and create your own"🙂, I found it a visually interesting representation of the interconnections of the profession and the passion.
Miyamoto Musashi (Author of Book of Five Rings) in one of his words says, "If you know the WAY broadly you will see it in everything" and being a passionate multi-year practitioner of the masters of fighting –the side of passion and by profession Power BI Report Creator al Data Analysit – the passion of the profession,   I considered it a combination - interesting interconnections between the fight sports events specifically UFC MMA Events in this case and analyzing them through the construction of a power bi report, where the results of the fights will materialize in order to tell the best story.
Given that there is more than one way up the mountain, at the moment, at this time, this is my way of moment that I saw fit to construct this report. I say this because the power BI's products are changing rapidly for the better, both on the surface – the visualization part as well as the content part, which is why we as creators try to keep up with the evolution of the product.  "Determine that today you will overcome your self of the day before"
## Data
The data were collected from several sources initially from VEGAS ODDS (there are csv files that for some reason are no more available), Wikipedia (extracted with web scrapping) as well as from the UFC official website (via webscrapping in this case pictures of the fighter). The initial records from Vegas Ods are very unclean. With power query, I've made it ready for date model. The initial purpose was that I considered these csv open to the public and the project was originally  built to download new files from Vegas Ods every week and the report is automatically updated. The date model built also followed a Header/Detail table approach by calculating the reusability of the data I had. This is no more available because that page does not pre-provide the information. The available data presents real data on ufc events held from March 11, 1994 to August 12, 2023 i.e. nearly 30 years since there are 7,128 fights. According to my analysis of the data, these data are not complete because some events are missing you can see it from the comparison of any fighter from my report and on the internet, but nonetheless those available are super enough for building a data model on which an event, fights and fighter  analysis report will be built.
As an idea in the future, I have to complete all the events through the construction of a PowerApps app or Google AppSheet Application for input data forms but it also depends on how much time I have available, always for myself and my curiosity.
The way to complete this report has some inspiration (from other platforms) that have served as the basis for further construction, while navigating the report is based on some reports I have seen by Miguel Myers (from him I have seen two levels, I have expanded them to three).
Due to the best use of the canvas I have used the tooltip as well as when I wanted to present details that I considered reasonable, I have used the drillthrough skillset in Power BI.

**_The purpose of this report is to reflect my skills as a data analyst and Power bi Creator in my portfolio and research the power bi capacities in presenting data in the form of a report approximately as web pages. The data is not my property and this report presentation has no commercial purpose, although the data presents the real competitions that have taken place (with some events like i mention abov eare lacking)._**

## Statement

Prompt:
I as a multi-year-old Martial Artist and Power BI consultant wanted to build for myself a model of data on the fights that take place in UFC-MMA for my own curiosity in order to analyze the conclusions of the lessons of where they come from and which ones dominate. The options for building the report in BI are numerous because there are abundant data, though not complete. 
  
## BI Requirements

The requirements of the bi project were analyzing these metrics:
- Number of events
- Event details
- Total Fights
- Total Finishes with KO/TKO
- Total Finishes with Submission
- Total Fights with Decision – Unanimous, Split, Majority
- Total Strike Attempt
- Total Strike Made
- Total Strike Significant
- Total Take Down Attempt
- Total Take Down Made
- Total Finishes (KO/TKO + Submissions)
- Total Decision (Unanimous + Split + Majority)
- Total Fighters
- Attempted Strikes vs. Strikes Made
- Attempted Take Downs vs. Take Downs Made
- Submission Attempt vs Submission Made
- Significant Strikes
- Target Strikest
- The type of strike that ended the Fight
- Type of Submission technique that ended the Fight

All the above as numbers and as percentages.

All these metrics should be analyzed in these dimensions: 

- Dim Calendar
- Dim Geography
- Dim Gender
- Dim Finish Type
- Dim Grouped Technique
- Dim Technique Details
- Dim Weight Class
- Dim Position
- Dim Executed From
- Dim Rounds
- Dim Title YES/NO
- Dim Result (Win - Loss)

Bus Matrix :
![](BusMatrix.png)

https://github.com/Paloja2017/UFC-Public-Power-BI-Report/assets/92805638/256c036b-e1cc-47ed-852a-cbff95446393
https://github.com/Paloja2017/UFC-Public-Power-BI-Report/assets/92805638/256c036b-e1cc-47ed-852a-cbff95446393


  
## Skills demonstrated

The project has been quite complex and challenging since the identification of the data that is complete, where I used Power Query to clean the data that was very dirty, web scraping on Wikipedia page and the UFC page as well as the use of GPT Chat for the needs during the progress of the project. Data modeling and DAX formulas where I used Tabular Editor 2 and 3 (especially C# macros).
Basic measurements as well as other measurements that are necessary and are presented specific to the project during the modeling process in a total of 225 complete measurements (counted in VertiPaq Analyzer) from functional measurements, measurements for automatic titles of visualizations, changes in color of visualizations, 4 columns added calculations and 3 calculation tables.
Most of the visualizations are native power bi visualizations, except for two that I used html content5 and Image Viz for the presentation of imagelinks as photos.
Tooltips were used intensively for the maximum use of the canvas, as well as for analyzing the details, I used the drillthrough where I wanted the details of the presentations, also in most of the visualizations, the drilldown is also present when I wanted to enter the dimensional hierarchy.
The navigation in the report is mainly two-level, but on some pages I have three levels without need, as can be seen when interacting with the report.















## Project Steps

- Identification of data sources
- Their extraction and purification
- Data residency in One Drive for Business
- Building the data model
- Building calculations and formulas in DAX
- Field Parameters
- Choice of navigation through the pages of the report
- The choice of visualizations that we consider suitable for showing the story
- The use of toltip for maximum use of the space of the canvas
- The use of drillthrough and drilldown for maximum use of the canvas space
- Refreshing them once a week - every Monday

- Created a new workspace named Fatjan Paloja Fabric_Test and selected a trial of Microsoft Fabric for 60 days.
  <br />
  <br />
 ![](Workspace_settings.png)

- Created a lake house
  <br />
  <br />
 ![](LakeHouse.png)
- Data source
  <br />
  Added new Data pipeline - TaxiDataPipeline_Directlake
  <br />
  <br />
![](PipelineData.png)
- Loaded to Delta table data preview
  <br />
  <br />
  ![](DeltaTablePreview.png)

- Linked a Pipeline to Outlook and Teams - on data refresh succes they sent a mesage you wrote beforehand, for example "Data is refreshed succesfully"
  <br />
  <br />
  ![](PipelinetoTeams.png)
  <br />
  <br />
- On SQL Endpoint I created a View and added new date only column
  <br />
  <br />
  ![](SQl_endpoint.png)

- Model view of storage mode as Datalake
  <br />
  <br />
   ![](DirectLakePicture.png)
  <br />
  <br />

- Modeling
  <br />
  Connected Power BI desktop to Onelake data hub - LakeHouses preview and loaded data as Direct Query over AS and for calendar table I used SqlBI Bravo tool which has builded for me Calendar Table with DAX (You can use a Calendar Table builded in Dataflow Gen2 also). I created relationship between Calendar Table and Taxi data on Date columns
  <br />
  <br />
![](DataModel.png)

- Measures, Calculated Table and Field Parameters
  <br />
  I have used VertiPaq Analyzer to list the measures for showing here. The procedure is to open the DaxStudio in Power BI external tools, in advanced tab export metrics, then connect Vertipaq Analyzer with .vpax file.
  <br />
  <br />
  ![](Measures.png)

## Visualizations:

  The report is single paged and intended for ease of use. We are measuring five metrics: Fare Amount, Average Trips Amount, Count of Trips, Tip Amount and Total Amount in single page - you can change the metrics in the slicer down right, also we have a slicer down left for selecting the years you want to analyze.
When you click a particular metrics slicer down right, that BAN number which is measured is highlighted. For the color I have choose #7B88BF to be in harmony with the fictional company logo.
  <br />

  ![](GifTest.gif)
    <br />
 ## Analysis:
By analyzing seven years of data, we see that NYC Taxis Company had more than 153 milion trips in total
|Year|Trips_#|              
|:----------|:----------|
|2013   |2,421,622|
|2014  |31,674,002|
|2015  |38,467,530|
|2016  |32,771,064|
|2017  |23,481,028|
|2018  |17,613,798|
|2019   |6,595,934|
   
As we see from data the year 2015 has maximum trips compared to other years with 38,467,530 also maximum transaction per month was in May2015 with 
3,573,696 trips
<br /> 
![](TripsAnalysis.png)
 
By analyzing seven years of data, we see that NYC Taxis Company had more than 1.90 Bn fare amount in total
|Year|Fare Amount $|              
|:----------|:----------|
|2013   |$ 30,038,429.24|
|2014  |$ 395,246,914.90|
|2015  |$ 474,342,003.48|
|2016  |$ 397,734,160.50|
|2017  |$ 276,958,721,38|
|2018  |$ 236,515,106.90|
|2019  |$ 90,187,147.06|
   
As we see from data the year 2015 has maximum fare Amount compared to other years with $ 474,342,003.48 also maximum fare amount per month was in May2015 with $ 45,470,410.92 dollars
<br /> 
![](FareAmount.png)


By analyzing seven years of data, we see that NYC Taxis Company has average of  $ 12.42  dollar per trip
|Year|Average Amount/Trip $|              
|:----------|:----------|
|2013   |$ 12.40|
|2014   |$ 12.48|
|2015   |$ 12.33|
|2016   |$ 12.14|
|2017   |$ 11.79|
|2018   |$ 13.43|
|2019   |$ 13.67|
   
As we see from data the year 2019 has greater average per trip compared to other years with $ 13.67 also maximum average per trip for year month was in Nov2018 with $ 14.42 dollars/Trip
<br /> 
![](AverageTrips.png)


By analyzing seven years of data, we see that NYC Taxis Company has in total $ 175.42 Milion dollar tips
|Year|Tips Amount $|              
|:----------|:----------|
|2013   |$ 2,138,815.32|
|2014   |$ 34,421,748,72|
|2015   |$ 46,718,194.34|
|2016   |$ 40,763,033.08|
|2017   |$ 26,995,782,82|
|2018   |$ 17,910,008.32|
|2019   |$ 6,476,652.96|
   
As we see from data the year 2015 has maximum Tips in dollars compared to other years with $ 46,718,194.34 also maximum ayear month was in May2015 with $ 4,572,791.96 dollars.
<br /> 
![](Tips.png)


By analyzing seven years of data, we see that NYC Taxis Company has more than $ 2.26 Bilion dollar total sales
|Year|Tips Amount $|              
|:----------|:----------|
|2013   |$ 34,549,295.16|
|2014   |$ 460,439,902.70|
|2015   |$ 570,883,021.18|
|2016   |$ 479,806,112.60|
|2017   |$ 334,415,882.20|
|2018   |$ 277,432,216.26|
|2019   |$ 107,378,070.30|
   
As we see from data the year 2015 has maximum amount in dollars compared to other years with $ 570,883,021.18 also maximum year month was in May2015 with $ 54,499,244.10 dollars.
<br /> 
![](Total.png)


![Taxis Company](https://img.shields.io/badge/Interact%20with%20Report-Taxis%20Power%20BI%20Report-ffbe0b?labelColor=7B88BF&style=flat&logo=PowerBI&logoColor=Yellow)

 
## Conclusion
 <br />
As we see from the data, trips reached maximum in 2015 and from there we have a decline with every year that passes. We have to analyze also some other data from other data sources and getting more and deeper insights about Sales Taxi Company.
This project as I mentioned above was only to experiment with Microsoft Fabric also to showcase some of Power BI capabilities. 

