<! DOCTYPE HTML>
<html>
	<head>
		<meta charset = "utf-8">
		<title>India COVID-19</title>
	</head>
	<style type="text/css">
		.title {
			text-align: center;
			text-decoration:underline;
			padding-top: 25px;
			font-family: all;
		}
		.corona{
			border-radius: 25px;
			cursor : pointer;
			width: 800px;
			display: block;
			margin-left: auto;
			margin-right: auto;
			box-shadow : 5px 5px 20px #ccc
		}
		h2 {

			text-decoration: underline;
		}
	</style>
	<body>
		
		<h1 class= "title">Data Analysis on COVID-19 in India</h1>
		<img src="https://user-images.githubusercontent.com/32237416/80790201-d35d5880-8bab-11ea-884b-41aa05119e18.jpeg" alt="COIVD Image" class="corona">
		<div class="intro">
			<h2> Introduction </h2>
			<p> On 31 December 2019 China first reported it’s Coronavirus in Wuhan, Hubei Province. A novel coronavirus was eventually identified, On 5 January 2020 WHO(World Health Organisation) announced an outbreak of coronavirus named it “COVID-19”, On 13 January 2020 Thailand reported the first COVID-19 case outside of china late WHO declared a worldwide health emergency.</p>
<p>In India, The country reported its first three
cases in Kerala, all of whom were students who
had returned from Wuhan , China. The
transmission escalated in March after several
cases were reported all over the country, most
of which were linked to people with a travel
history to affected countries. On 10 March, the
total cases reached 50. On 12 March, a 76-yearold man who had returned from Saudi Arabia
became the first victim of the virus in the
country. The total cases reached 100 on 15
March and 250 on 20 March and by April 30 the
country reported 35365 total, 9065 cured, and
1152 death cases.</p>
		</div>
		<div>
			<h2>Problem</h2>
			<p> Even though many websites give a clear insight
into a pandemic in India. I want to create a
simple insight into the outbreak using python
scripting language from pandas, matplotlib,
folium libraries.</p>
<h3> Exploring Datasets </h3>
<p>The data set is available from the “Ministry of
Health and Family Welfare” <a href= "https://
mohfw.gov.in"> Website </a>  where we have to explore which
data set is suitable for our requirement.</p>
<h3>Downloading and Prepping</h3>
<p>Data downloaded or scraped from “Ministry of
Health and Family Welfare” <a href= "https://
mohfw.gov.in"> Website </a>  and I have collected Indian
states latitude and longitude from google maps
as to plot the geospatial visualisation
of corona cases throughout the country, after
scrapping the data into DataFrame using pandas
library, I've observed that data should be
prepared for further stages as a part I have
removed last three unwanted rows from the data
frame and there only three columns which
indicate cured, death,& total however for a
better solution I have added another column
“Active” for better understanding I have
changed names the columns from {Name of State /
UT': 'State/UT', 'Total Confirmed cases
(Including 111 foreign Nationals)’:’Total',
‘Cured/Discharged/Migrated’:’Cured’}.</p>
		</div>
		<div>
			<h3>The Total States Affected by COVID -19</h3>
				<p>As of 30 April 2020 26 states & 6 union
territory have been affected with corona virus,
in pandas using groupby attribute I have sorted
in descending ordered from the data frame and
plot as below using matplotlib.</p>
<figure class="fig">
<img src="Images/fig1.png" alt="Total States">
<figcaption>Bar graph of affected states by corona</figcaption>
</figure>
</div>
<div>
<h3> Top 5 states affected by COVID-19</h3>
<p>As we know from the data Maharashtra, Gujarat,
Delhi, Madhya Pradesh, & Rajasthan are being
top 5, as we know the incident(Tablighi Jamaat)
happen in Delhi on before lockdown as there is
more crowd in the incident as they have
traveled throughout the country and government
recognised it as coronavirus super-spreader
event, with more than 4,000 confirmed cases and
at least 27 deaths linked to the event reported
across the country.</p>
<figure>
<img src="Images/fig2.png" alt="Top 5 states">
<figcaption>Area plot of Top 5 states affected by corona virus</figcaption>
</figure>
</div>
<div>
	<h3> Least affected states </h3>
	<p>Goa, Tripura, Manipur, Mizoram, Arunachal
Pradesh are the least affected states by the
coronavirus in the country. 7 corona cases in
Goa, 2 corona cases in Tripura & Manipur, 1
case in Arunachal Pradesh.</p>
<figure>
<img src="Images/fig3.png" alt="Least affected">
<figcaption>Least affected states</figcaption>
</figure>
		</div>
		<div>
			<h3>Active cases in India</h3>
			<p>As of 30 April 2020, there are 19 states with
25,148 active cases whereas remaining states 13
states have no active out of 32 states that
have been reported corona cases in the country.</p>
<figure>
<img src="Images/fig4.png" alt="Active cases">
<figcaption>Active cases in India</figcaption>
</figure>
	</div>
	<div><h3>Top 5 Active States</h3>
		<p>As we know from the data set Maharashtra,
Gujarat, Delhi, Madhya Pradesh, & Rajasthan are
being top 5 as they have high corona cases and
it will take almost 2 weeks to recover from
coronavirus, as there is a recent spike in all
these states which might lead to being a high 
chance of spreading coronavirus in these
states.</p>
<figure>
<img src="Images/fig5.png" alt="Active states">
<figcaption>Top 5 Active States</figcaption>
</figure>
</div>
<div><h3>Have low impact by Covid-19</h3>
		<p>As these states have a low chance of spreading
coronavirus due to knee-high corona cases.</p>
<figure>
<img src="Images/fig6.png" alt="low impact">
<figcaption> Low Impact states</figcaption>
</figure>
</div>
<div><h3>Cured patients from Covid-19 </h3>
		<p>As of 30 April 2020, there are 27 states with
9065 cured cases whereas remaining states 5
states have already rehabilitated out of 32
states that have been reported corona cases so
far in the country. </p>
<figure>
<img src="Images/fig7.png" alt="‘Cured states">
<figcaption>Rehabilitating States</figcaption>
</figure>
</div>
<div><h3>Fast Rehabilitating States</h3>
		<p>In some states, the rate rehabilitating is very
high because of the affected patients mostly
under 60 years age group, as per WHO it is said
that under 60 years age the patients who are
attacked by coronavirus should be kept in
isolation treatment for 2 weeks if they have no 
other disease there is a high chance of getting
rehabilitated quickly, as per the data set
Maharashtra, Tamil Nadu, Delhi, Rajasthan, &
Gujarat have a high recovery rate than compared
to other states in the country.</p>
<figure>
<img src="Images/fig8.png" alt="Rehabilitating states">
<figcaption>Fastest recovering States</figcaption>
</figure>
</div>
<div><h3>Deaths by COVID-19 </h3>
		<p>The country has 1152 deaths as of April 2020,
as we know under 60 years of age group or who
have low immunity or suffering from various
diseases have a high chance to die by the
coronavirus, as the country has a more young
population than the old country is seeing low
death rate by a coronavirus. </p>
<figure>
<img src="Images/fig9.png" alt="Active states">
<figcaption>Area Plot of Deaths</figcaption>
</figure>
</div>
<div><h3>High Death Impact states</h3>
		<p>Maharashtra share 45% death percentage followed
by Gujarat, Madhya Pradesh, Delhi, & Rajasthan. </p>
<figure>
<img src="Images/fig10.png" alt="High Death states">
<figcaption>High Death</figcaption>
</figure>
</div>
<div><h3>No Death Impact </h3>
		<p>Puducherry, Ladakh, Mizoram, Uttarakhand, &
Andaman and Nicobar Islands have not reported
any death by coronavirus so far.</p>
<figure>
<img src="Images/fig11.png" alt="No death">
<figcaption>No Death</figcaption>
</figure>
</div>
<div><h3>Regression Plot between Active and Total </h3>
		<p>Even though we know that, if total cases
increase the active cases will also increase,
to better understand the data from data set
between active cases and total corona cases I
have used the regression plot.
In the regression plot, we can see a straight
line passes through the active cases and total
cases in India.</p>
<figure>
<img src="Images/fig12.png" alt="Regression Plot">
<figcaption>Regression Plot</figcaption>
</figure>
</div>
<div><h3>Area Plot </h3>
		<p>As my native place is Telangana I want to
compare Telangana data with other top 3 states
in the country. From the data we can conclude
that Telangana has fewer corona cases compared
to the other three states as 30 April 2020.</p>
<figure>
<img src="Images/fig13.png" alt="Active states">
<figcaption>Telangana Vs MH, TN, GJ</figcaption>
</figure>
</div>
<div><h3> Geo-Spatial Visualisation</h3>
		<p>I have collected latitude and longitude numbers
of Indian states scraped from google maps and
created into pandas data frame later using
merge attribute I have merged data frame from
the MOHFW website into a new data frame, using
folium library I have plotted on maps.
It will give a glance at every state. </p>
<figure>
<img src="Images/fig14.png" alt="Active states">
<figcaption>GeoSpatial Visualisation of COVID</figcaption>
</figure>
</div>
<h3>Conclusion</h3>
<p>In this study,I have analyzed coronavirus cases
in India in various visualization like a bar
graph, area plot, line plot, regression plot, &
geospatial in every column from the data frame,
even though the data is easily available in the
public domain as recently I have learned Data
Analysis I would like to apply it on real-time
data. From this data set, I came to Know that
for better analysis time series should be used.</p>
	</body>
</html>
