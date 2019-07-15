# Homework-20_City-Bike-Analytics

<p><strong>This project aims to generate report for the <a href="https://en.wikipedia.org/wiki/Citi_Bike">New York Citi Bike</a> Program using data from <a href="https://www.citibikenyc.com/system-data">Citi Bike Data</a>. Specifically, data used here are monthly trip data between 2017/06 and 2019/05 and quarterly trip data from the third quarter of 2018 to the second of 2019. The historical monthly temperature data of the same quarter periods for Central Park, NY was obtained from <a href="https://w2.weather.gov/climate/index.php?wfo=okx">National Weather Service Forecast Office, New York, NY</a>.</strong></p>

<p><strong>Tableau .twbx file has been uploaded to Tableau Public, in which all <i>Worksheets</i> has been hided to only show <i>Dashboards</i> for visualization. Names of <i>Worksheets</i> can be seen at left side of the <i>Dashboards</i> under <i>Sheets</i> and be accessed from there by hovering on <i>Worksheets</i>' name and click "Go to Sheet" button. Viz can be accessed <a href="https://public.tableau.com/profile/lei8768#!/vizhome/NYCCitiBikeAnalytics/DBRidershipinGeneral?publish=yes">here</a></strong>.</p>

<h3>Ridership in General</h3>

<p>As compared to that in Jul 2018, the monthly ridership exhibited a 3.35% increase in Aug 2018, which gradually but steadily decreased month-by-month towards the groove in Jan 2019 (with a negative growth percentage). From then on, the monthly ridership started to climb up until the end of our sampling period (Jun 2019). Such trends echoed perfectly to that of New York City temperature (as represented by temperature of Central Park, NY), indicating a correlation between ridership and temperature.</p>
<img src="/data/figures/readme-images/ridership-in-general.png" alt="ridership in general">
  
<h3>Ridership by Hours</h3>

<p>In calculating the membership purchases people made to Citi Bike in the latest 12 months, I found that annual subscribers were gradually increasing throughout the entire period whereas short-term customer purchases (both 24-hour and 3-day pass) showed a similar pattern as that of the general ridership discussed above.</p>
<img src="/data/figures/readme-images/ridership-by-users.png" alt="ridership by users">

<p>Taking the latest month with available data (Mar 2019) into detailed study, I figured out that the average hourly ridership formed "M" shape distribution. The ridership reached to the average point of the day between 6 and 7am, which stayed above the average line, with two peaks at 8am and 5pm, respectively, and a groove between 10 to 11am, until later than 8pm. Specifically, annual subscribers followed the same distribution pattern. Average ridership for short-term customers, on the other hand, formed a parabola shape, first touching the average line 3 hours later (between 9 and 10am) than the "M" shape distribution, keeping increasing to peak around 3pm, and going under average line after 8pm. "M" and parabola distributions of ridership reflect the behaviors of two totally different cohorts of Citi Bike users.</p>
<img src="/data/figures/readme-images/ridership-by-hours.png" alt="ridership by users"> 

<h3>Ridership by Genders</h3>

<p>Another way to interpret the ridership data is to look at the gender distribution. As seen from the chart of <i>Percentage of Female and Male Ridership between 2017/06 and 2019/05</i>, the intermediary line between Male% and Female% looked like an upright sinusoid, with Female% / Male% peaking in September and Male% / Female% peaking in January. Taking unknown gender (8.8%) into consideration, males accounted for two thirds of all users. The figure for females was around one quarter. While gender distribution on weekdays remained pretty much the same, interestingly, it was not the case for that on weekends. Although the percentage for females did not change, that for males dropped by 8%, which in turn contributed for the increase in unknown gender. It is the evidence suggesting a trend that some males were reluctant to release their gender info when using Citi Bike on weekends.</p>
<img src="/data/figures/readme-images/gender-distr-ridershp.png" alt="ridership by users"> 

<h3>Trip Duration by User Ages</h3>

<p>Arbitrary inputs of user year of birth (YOB) info were identified during analysis of Citi Bike data. To facilitating data visualization, I set up the starting point of YOB to be at age of 90. Any YOB data that was earlier than it was set as 1910. There were also data in 2017 that were missing YOB info. Such data were given the YOB of 1900. While dragging the "YOB" filter, it was clear on the chart of <i>User YOB Counts between 2017/06 and 2019/05</i> that there were a huge amount of undocumented YOBs in 2017, which completely dropped to 0 from 2018/01. At the same time, an abnormally large bunch of YOB 1969 counts showed up. The count of greater than 90 YOB remained largely unchanged with a value below 2000. Since the percentages of undocumented and older than 90 YOBs among all monthly YOB counts were equal or relatively close to 0, I made a circle plot of sum YOB% of "1900", "1910", and "1969" on top of the line charts, only to find harmonious plotting patterns for all users (sinusoid), as well as for short-term customers (linear with slightly negative slope) and annual subscribers (horizontal line). After 2018/01, the line of YOB=1969 coinsided with the circles in all charts. As a result, there might be the possibility that there are the same group of people standing behind the undocumented, greater than age of 90, and extremely high YOB=1969 counts, who were forced to swing from not giving YOB info in 2017 to YOB=1969 afterwards.</p>
<img src="/data/figures/readme-images/user-yob-counts.png" alt="ridership by users">   

<p>There are extreme peaks on chart of <i>Trip Duration by Ages</i>, being duration for the age of 16, 50, 84, and 88. While looking at the case distribution of extreme ages, I identified two outliers: one in age of 16 with duration of 13441 min and the other one from age of 88 with duration of 176.4 min. In Updating the trip duration chart by removing two outliers, there were still three extreme high values at the age of 50 (YOB=1969, could not be further analyzed in current scenario), 84, and 88 (unreasonable, age threshold of 90 might be set lower). Apart from that, younger users tent to ride longer than older one between the age of 16 and 40. It became flat after 40. The trend was almost the same on weekdays. However, there were more random high peaks before 50 on weekends. Users in general were riding longer than on weekdays.</p>
<img src="/data/figures/readme-images/duration-by-age.png" alt="ridership by users"> 
  
<h3>Operation and Cost-effectiveness</h3>

<p>The top 10 start and end stations by counts were all located in middle and south part of Manhattan, whileas the bottom 10 stations were mostly satellited outside on map. Station <strong>9 Ave & W 22 St</strong> was listed in bottom 10 of both start (ct=36) and end (ct=8) stations. What made it worse is that the station locates in Manhattan, surrounded by top 10 stations. A closer attention and discussion over this station might be needed from the perspective of operation and cost-effectiveness.
<img src="/data/figures/readme-images/ridership-by-tb10-start-sta.png" alt="ridership by users"> 
<img src="/data/figures/readme-images/ridership-by-tb10-end-sta.png" alt="ridership by users"> 
