80% of this work is done by me.
The Sustainability team was interested to make a warning system that could predict if the smoke of wildfire is getting closer to their infrustures and client's buliding and if so, how fast is the smoke improvement and find out the best time for evacuation in order to keep the occupants healthy.
As this was first time doing such a project, I researched for the most important factors in the smoke that affect people's health and then include other variables to the next version. 
Research showed me that PM 2.5 is one of the most plontents in smoke. Therefoe I use Airnow.gov api to get the north america's somke data for everyday. This data were captured from various towers wich each were distinguisged with a unique AQSID.
Afterwards I cleand the data and took an average for every tower for the day before and called the table "Yesterday".
Then merged it with our Building data on Building_ID. I gave the PM 2.5  towers a Building_ID as well. 
Then found the nearest neighbour tower ( up to 1000 km) to each buliding and gave the value of PM 2.5 to that building, using haversine formula and lattitude and longtitute.
After some cleaning, binned the amount of P.M 2.5 allocated to each building to categories from healthy, Moderate,... Hazordous based on resources.
Then some alterations were made and the final result was saved in a csv file.
Each csv file was pulled everyday to our dashboard.
I made the dashboard in a way that we could see everyday, how many buildings in each state/province are expriencing healthy/undealthy/dangrous/ air quality or mapped them out on a GIS map and other various categories and investigations.


![Air Quality](Smoke_Dashboard.jpg)
![Air Quality](Smoke_Dashboard2.jpg)