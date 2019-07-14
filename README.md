# Homework-20_City-Bike-Analytics

<p><strong>This project aims to generate report for the <a href="https://en.wikipedia.org/wiki/Citi_Bike">New York Citi Bike</a> Program using data from <a href="https://www.citibikenyc.com/system-data">Citi Bike Data</a>. Specifically, data used here are monthly trip data between 2017/06 and 2019/05 and quarterly trip data from the third quarter of 2018 to the second of 2019. The historical monthly temperature data of the same quarter periods for Central Park, NY was obtained from <a href="https://w2.weather.gov/climate/index.php?wfo=okx">National Weather Service Forecast Office, New York, NY</a>.</strong></p>

<h3>Ridership in General</h3>

<p>As compared to that in Jul 2018, the monthly ridership exhibited a 3.35% increase in Aug 2018, which gradually but steadily decreased month-by-month towards the groove in Jan 2019 (with a negative growth percentage). From then on, the monthly ridership started to climb up until the end of our sampling period (Jun 2019). Such trends echoed perfectly to that of New York City temperature (as represented by temperature of Central Park, NY), indicating a correlation between ridership and temperature.</p>
<img src="/data/figures/readme-images/ridership-in-general.png" alt="ridership in general">
  
<h3>Ridership by Hour</h3>

<p>In calculating the membership purchases people made to Citi Bike in the latest 12 months, I found that annual subscribers were gradually increasing throughout the entire period whereas short-term customer purchases (both 24-hour and 3-day pass) showed a similar pattern as that of the general ridership discussed above.</p>
<img src="/data/figures/readme-images/ridership-by-users.png" alt="ridership by users">

<p>Taking the latest month with available data (Mar 2019) into detailed study, I figured out that the average hourly ridership formed a "M" shape distribution. The ridership reached to the average point of the day between 6 and 7am, which stayed above the average line until later than 8pm.

  
<br>Tableau .twbx file has been uploaded to Tableau Public, in which all <i>Worksheets</i> has been hided to only show <i>Dashboards</i> for visualization. Viz can be accessed <a href="https://public.tableau.com/profile/lei8768#!/vizhome/NYCCitiBikeAnalytics/DBRidershipinGeneral?publish=yes">here</a>.
