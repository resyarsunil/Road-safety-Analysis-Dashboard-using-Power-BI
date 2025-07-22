# Road-safety-Analysis-Dashboard-using-Power-BI
I developed a comprehensive project in Power BI, Creating multiple KPI's and charts to analyze the data. This Process involved several stages, including data cleaning, data processing, data modeling and data visualization. So, this dashboard highlights key metrics, trends, and comparisons making it powerful tool for strategic decision making.

#1. Data Cleaning and Preprocessing
• Spelling Correction: During the data cleaning process, a key correction
involved fixing a typographical error in the Accident Severity column. All
instances of “fetal” were corrected to the appropriate term “fatal” to maintain
data integrity and consistency.

#2. Data Modeling and Transformation
• Grouping of Vehicle Types: Similar vehicle types were grouped into broader
categories for better analytical clarity:
o Car
o Bus
o Van
o Agricultural vehicle
o Motorcycle
o Other
• Light Conditions Consolidation:
o Day
o Night (includes “Darkness – lights lit”, “Darkness – lights unlit”, etc.)

## Steps Followed

1. A new calendar table is created which contains the date, year, day of week.
2. For calender table, Table = CALENDAR(MIN(Data[Accident Date]),MAX(Data[Accident Date]))
3. For year, Year = YEAR('Table'[Date])
4. For day in number, day = WEEKDAY('Table'[Date])
5. Additionally, DAYS1 = FORMAT('Table'[Date],"DDDD")~ It is used for findind the Day of the week trend
6. Total 2021 Casualties 2 = CALCULATE(SUM(Data[Number_of_Casualties]),'Table'[Year]=2021)
7. Total 2022 casualties 1 = CALCULATE(SUM(Data[Number_of_Casualties]),'Table'[Year]=2022)
8. Year on year Casualties = ([Total 2022 casualties 1]-[Total 2021 Casualties 2])/[Total 2021 Casualties 2]

## Requirements


1. Visual filters (Slicers) were added for two fileds named "Accident_severity" and "Year".
2. Five Primary KPI's such as:
   -Total Accidents ( Calculated using index)
   - Total Casualties
   - Total Fatal Casualties
   - Total Severe Casualties
    - Total Slight Casualties

3. Two Secondary KPI's such as:
   - Total casualties in rural areas
   - Total casualties in urban areas
  
4. Accidents by Road surface condition (Multi row card)
5. Casualties by light condition (Donut chart)
6. Casualties by Road type ( Donut chart)
7. Casualties by vehicle type ( clustered Bar chart)
8. Day of the week Casualties trend ( Area chart)


   ## KEY FINDINGS

   1. Accident Severity Distribution:
A year-over-year comparison between 2021 and 2022 indicates a positive
downward trend in road accidents and related casualties. The total number of
accidents decreased by 11.7% in 2022 compared to the previous year.
Similarly, overall casualties saw an 11.9% reduction. Notably, fatal casualties
experienced a significant decline of 33.3%, while serious casualties dropped
by 16.2%. Slight casualties also decreased by 10.6%. These reductions suggest
potential improvements in road safety measures, enforcement, or public
awareness; however, further analysis is needed to determine the specific
factors contributing to this decline.

2. Vehicle Type Impact:
o Motorcycles and Car were more frequently involved in serious and fatal
accidents compared to other vehicle types.

3. Light Condition Influence:
o Daylight conditions showed a higher number of accidents.

4. Geographical Distribution:
Accident frequency was found to be higher in urban areas compared to rural regions.
This may be attributed to increased traffic density, congestion, and frequent
interactions at intersections in city environments.


5. Accident Distribution by road type
An analysis of total accidents by road type revealed that 74.9% occurred on
single carriageways, making it the most common road type for accidents.
This was followed by dual carriageways with 14.7%, and roundabouts
accounting for 6.8%, with the remaining percentage distributed across other
road types.

6. Day of the Week Casualties Trend:
   Saturday had the highest number of road casualties in both 2021 and 2022, indicating increased risk during weekends. Sunday consistently recorded the lowest casualties,
    possibly due to reduced travel or more cautious driving. There was a noticeable decline in casualties in 2022 compared to 2021 across all days of the week (down 11.9%).


7. Regarding accidents by road surface condition: The data reveals that the majority of accidents occurred on dry roads (208,967 cases), accounting for nearly 68% of the total. This suggests that favorable weather and road conditions do not eliminate accident risks, and factors like speeding, distraction, or negligence likely play a major role. Wet or damp surfaces were the second most common condition (81,796 accidents), highlighting the danger posed by slippery roads. Accidents on frost or ice (12,078) and snow-covered roads (4,758), while fewer in number, remain critical in specific regions or seasons. Interestingly, flood conditions accounted for the fewest accidents (374), possibly due to road closures or drivers avoiding travel during such events.



## Insights derived.

   Improved Road Safety Trends: The notable year-over-year decrease in total
accidents and casualties suggests that road safety interventions, law
enforcement efforts, or increased public awareness may be contributing to
positive outcomes. However, continued monitoring and analysis are essential
to sustain and enhance these improvements.
• High-Risk Vehicle Categories: Motorcycles and cars are disproportionately
involved in serious and fatal accidents. This indicates a need for targeted safety
measures such as stricter helmet and seatbelt enforcement, rider/driver
education programs, and vehicle safety audits.
• Daylight Accidents Require Attention: Although accidents are often expected
to be more severe at night, the higher volume of accidents during daylight
hours indicates that distraction, traffic congestion, and overconfidence during
clear visibility might be contributing factors. Daytime safety campaigns and
better traffic control during peak hours could be effective.
• Urban Traffic Management: The higher frequency of accidents in urban areas
highlights the need for improved traffic management systems, pedestrian
safety infrastructure, and congestion mitigation strategies in cities and towns.
• Road Design Considerations: The dominance of single carriageway roads in
accident occurrences (74.9%) suggests that these roads may lack sufficient
safety features such as dividers, warning signage, or proper lane markings.
Investing in the redesign or enhancement of single carriageway roads could
significantly reduce accident rates.
• Weekend and late-week driving (especially Friday and Saturday) are associated with higher 
risks—possibly due to leisure travel, fatigue, or increased traffic volume.
• While poor weather conditions are risky, most accidents happen in normal (dry) conditions, suggesting driver behavior, 
speeding, and distraction are primary causes—not just weather.








