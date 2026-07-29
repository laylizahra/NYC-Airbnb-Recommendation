# NYC-Airbnb-Recommendation
New York City Airbnb Recommendation 

## Project Overview 
This project inform an Exploratory Data Analysis (EDA) on Airbnb in New York City to understand the key factors that influence listing prices. The analysis aims to build actionable insights for both prospective tenants looking for suitable home and potential investors evaluating opportunities in the short-term market. 

## Background 
Airbnb has become a growing platform for short-term property rentals, especially in major cities such as New York. New York City represents a big city with one of the largest and competitive Airbnb markets in the world with thousands of active listings varying widely in price, room type, and location. However, listing prices in this market showing wide variation from budget-friendly rooms to premium rooms costing thousand of dollars for each night. 

## Goals 
1. Analyzing the key factors that drive Airbnb price variation in New York City, such as location, room type, bedrooms, and availability.
2. Providing data-driven recommendation for tenants to help finding rooms that match their budget and preferences.
3. Identifying the most promising boroughs and room types for potential Airbnb opportunities.

## Dataset 
- *Source:* New York City Airbnb Listing 2024 by Zero Analyst on Youtube
- *Size:* 20.770 rows x 22 columns 
- *Key Variables used:* 'price', 'room_types', 'neighbourhood_group', 'availability_365', 'beds', 'bedrooms', 'number_of_reviews'
- *Missing values:* Most key columns have fewer than 35 missing rows out of 20,770 (under 0.2%), handled via row removal without meaningfully affecting results.
- *Outliers:* The `price` column contains extreme outliers (up to $100,000/night). These were capped at the 99th percentile for visualization to avoid distortion while preserving the overall distribution shape.

## Key Findings

**1. Room Type Distribution**
Entire home/apartment (55%) and private room (42%) dominate the market, together making up over 95% of all listings. Shared rooms and hotel rooms are niche categories.


**2. Price by Borough**
Manhattan has the highest median price ($150/night), followed by Brooklyn ($125), while Queens, Bronx, and Staten Island offer more budget-friendly options (median $89–99/night).

**3. Correlation Heatmap**
Price shows very weak correlation with availability (0.02), number of reviews (-0.01), and beds (0.07). Suggesting these factors alone do not meaningfully drive pricing. Bedrooms proved to be a stronger price predictor than beds.

**4. Price Distribution**
Prices are heavily right-skewed (skewness ≈ 90), with the mean ($187) well above the median ($125), driven by a small number of extremely high-priced listings.

**5. Host Listing Count Analysis**
Hosts managing many listings (likely property management companies, up to 146 listings) tend to price more competitively (lower median) than casual hosts with a single listing, suggesting a volume-based pricing strategy.

## Best Locations & Recommendation 
Based on the borough level price analysis, here are location recommendation to different audiences: 

*For Tourists (short-term stay, location focused):*
Manhattan or Brooklyn -- Entire home or apartment or private room 
- Tourist typically looking for a rent near attractions, making Manhattan (median $150) the most sensible choice despite the higher cost, it offers easy access to landmarks and public transit. 
- Brooklyn (median $125) is another good option for a more budget-friendly option that still close to city centre, especially in a trendy area like Williamsburg.
- Room type: entire home/apt for family or groups, while private room suits for solo travelers with tighter budget.

*For Students (Limited budget, mid-term stay)*
Queens or Bronx -- Shared room or private room
- Mostly, students budget are tight, this making Queens or Bronx (median $89 - $99) are the most realistic choice.
- Room type: private room offers privacy at a lower price than an entire home. For very limited budgets, shared room is also an option though the availability is scarce (only 293 listings)

*For Working Professionals (Business trip or Relocation)*
Manhattan or Brooklyn -- Entire home or apt
- For short business trip, Manhattan entire home/apt is ideal because near business districts, minimal distractions, and full privacy.
- For medium-term work relocation (several months), Brooklyn offers a more economical option while maintaining good quality of life, with many highly-rated listings in areas like Park Slope and DUMBO.
- Room type: Entire home/apt is preferred since work needs typically require a quiet space (WFH-friendly) and full privacy rather than a shared living situation.

*For Families (need more space)*
Queens or Staten Island -- Entire home or apartment with multiple bedrooms.
- As shown in the bedroom-price analysis, prices increase significantly with bedroom count (2-bedroom: $181, 3-bedroom: $249). Families needing more space get the best value in Queens/Staten Island — lower per-night prices allow for larger properties compared to the same budget in Manhattan.
- Staten Island is also quieter and more residential, making it well-suited for families who don't need constant urban activity.

*For Budget-Travelers or Backpackers*
Bronx -- Private or shared room
- Bronx consistently shows the lowest prices (median $89) with the narrowest interquartile range, indicating more stable and predictable pricing with fewer unexpectedly expensive listings.
- For travelers flexible on location and willing to commute further via public transit, this is the most cost-effective option.






