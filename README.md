# Airline Passengers Satisfaction Analysis | PowerBI

This project analyzes airline passenger satisfaction using Power BI to identify key factors affecting customer
experience. It leverages survey and operational data, visualizing trends to provide actionable insights for enhancing
service quality, customer retention, and overall satisfaction.

# Airlines-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/a1a23456-5f6e-4c2c-b97e-9c78cffeeb3e/2583c0c08ca09d61b105?experience=power-bi

## Problem Statement

This dashboard provides airlines with valuable insights into customer satisfaction. By analyzing various ratings, airlines can pinpoint areas needing improvement and enhance their services accordingly. Additionally, the dashboard tracks average delays and departure times, helping airlines identify recurring issues. With this data-driven approach, they can address the factors causing delays and work towards providing a smoother travel experience.

With nearly 57% of customers being neutral or dissatisfied compared to around 43% who are satisfied, it’s clear that improvements in service are needed.

Additionally, since both arrival and departure delays average 15 minutes, efforts should be made to minimize these delays


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Arrival Delay".
- Step 5 : For calculating average delay time, null values were not taken into account as only less than 1% values are null in this column(i.e column named "Arrival Delay") 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields named "Class", "Customer Type", "Gate Location" & "Type of travel".
- Step 9 : Two card visuals were added to the canvas, one representing average departure delay in minutes & other representing average arrival delay in minutes.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing the number of satisfied & neutral/unsatisfied customers. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of customers are also seggregated according the gender. 
- Step 11 : Ratings Visual was used to represent different ratings mentioned below,

  (a) Baggage Handling

  (b) Check-in Services
  
  (c) Cleanliness
  
  (d) Ease of online booking
  
  (e) Food & Drink
  
  (f) In-flight Entertainment

  (g) In-flight Service
  
  (h) In-flight wifi service
  
  (i) Leg Room service
  
  (j) On-board service
  
  (k) Online boarding
  
  (l) Seat comfort
  
  (m) Departure & arrival time convenience
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 12 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them name of the airlines was mentioned & in the other one company's tagline was written.
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 
- Step 14 : Calculated column was created in which, customers were grouped into various age groups.

Snap of conditional column used to make new column in
power query,
       
![Image](https://github.com/user-attachments/assets/4744f3ee-b58f-48ab-9b51-190297b6ba43)
        
Snap of new conditional column ,

![Image](https://github.com/user-attachments/assets/81c99dc9-116d-4b7f-8d19-631d90d90816)


        
- Step 15 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        
A card visual was used to represent count of customers.

![Image](https://github.com/user-attachments/assets/a9ddedff-85f0-4a01-a695-8cb6e8794281)

        
 - Step 16 : New measure was created to find Average flight distance,
 
 Following DAX expression was written to find Average flight distance,
 
         Average flight distance = AVERAGE(airline_passenger_satisfaction[Flight Distance]
 
 A card visual was used to represent this perecntage.
 
 Snap of Average flight distance
 
![Image](https://github.com/user-attachments/assets/7e3b006e-75de-4aca-8130-ae29d487feb3)

 
 - Step 17 : New measure was created to calculate Average Departure Delay
 
 Following DAX expression was written to findAverage Departure Delay,
 
         Average Departure Delay = AVERAGE(airline_passenger_satisfaction[Departure Delay]

 A card visual was used to represent this total distance.
 
 
 ![Image](https://github.com/user-attachments/assets/9193aeca-1cde-4186-9c61-5cc5c345d317)
 
 - Step 18 : The report was then published to Power BI Service.
 

# Snapshot of Dashboard (Power BI Service)

![Image](https://github.com/user-attachments/assets/6ab5f3cd-27b8-4dff-a09c-29c4387144e5)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Image](https://github.com/user-attachments/assets/42db786c-cf18-4baa-8464-806f5820832d)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
