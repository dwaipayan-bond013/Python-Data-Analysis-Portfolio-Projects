# OLA Ride Analysis
<p align="center">
<img src="ola-case-study.jpg" width="1000"/>
</p>

---

## Project Overview
The OLA Ride Analysis project is a data-driven initiative focused on optimizing ride-sharing operations through comprehensive analysis of historical usage patterns. In today’s fast-paced urban mobility landscape, understanding user behavior, driver dynamics, and operational efficiency is critical for delivering timely, reliable, and cost-effective transport services. This project addresses these challenges by dissecting key aspects of the OLA platform’s ride data at an hourly resolution.

## Dataset Overview

The core dataset captures user interactions and driver activities over a series of time intervals, providing a granular view of how the ride-sharing ecosystem behaves across different hours of the day. By examining variables such as the number of users who opened the app (Eyeballs), number of ride requests, trip completions, and availability of drivers, the analysis uncovers systemic gaps and opportunities for strategic improvement.

| Column            | Description                                      |
| ----------------- | ------------------------------------------------ |
| `Time (Local)`    | The hour of the day (0 to 23)                    |
| `Eyeballs`        | Number of users who opened the OLA app           |
| `Zeroes`          | Number of users who didn’t see any available car |
| `Requests`        | Number of ride requests made                     |
| `Completed Trips` | Number of rides successfully completed           |
| `Unique Drivers`  | Number of drivers logged in during that hour     |

This project serves multiple use cases for stakeholders including:
  - Operations teams, to optimize supply planning
  - Product teams, to improve app engagement and reduce abandonment
  - Marketing teams, to identify drop-off points and personalize offers
  - Drivers, to increase earning potential through better timing and positioning

## Insights and Analytics

1. ![](TripRequestHourlyAnalysis.PNG)

- Business Insights:
  - Strong evening and late-night demand – indicative of work returns, events, and nightlife (11 PM (23:00): 184 requests, 7 PM (19:00): 156 requests)
  - **5 PM to 2 AM** shows a consistent volume between 96–112 requests
  - Early night hours still show significant demand, requiring continued driver availability
  - **4 AM (9 requests)** and **5 AM (14 requests)** mark the lowest activity
  - Indicates low operational urgency but potential for targeted niche service (e.g., airport rides)
  - From **9 AM to 5 PM**, request volume steadily increases.

- Business Implications & Recommendations

| Area                   | Recommendation                                                                  |
|------------------------|---------------------------------------------------------------------------------|
| **Driver Allocation**   | Prioritize driver logins during **5 PM – 1 AM**.                               |
| **Dynamic Pricing**     | Apply surge pricing in **6 PM – 12 AM** window to manage high demand.          |
| **Driver Incentives**   | Offer night-time bonuses to improve supply between **10 PM – 2 AM**.           |
| **Customer Experience** | Communicate expected ETAs and price changes during peak hours via app banners. |
| **Marketing Campaigns** | Run early-morning offers (3–7 AM) to boost off-peak demand.                    |
| **Operational Strategy**| Use demand prediction to move idle drivers toward high-demand zones.           |


2. ![](DriverAvailabilityvsRequestedTrips.PNG)

- Business Insights:
  - Late Night & Early Morning (0:00–5:00)
     - Demand (Requests) is relatively high at 23:00 (184),00:00 (142) and 01:00 (96) but drops sharply from 2:00 to 5:00
     - Driver availability matches well, with a slight oversupply from 03:00–05:00, e.g.: 04:00: 9 requests vs 9 drivers (balanced)
     - There's a decent balance, though a slight under-supply during late-night rush (12 AM–2 AM) 
  - Morning Hours (6:00–11:00)
     - Driver count rises rapidly starting at 6 AM, reaching 129–133 between 10–12 AM, but requests remain low, e.g.: 09:00: 26 requests vs 110 drivers, 10:00: 28 requests vs 129 drivers
     - Significant driver over-supply during morning hours. Drivers may be idle or underutilized
  - Afternoon Hours (12:00–17:00)
Supply remains high (~120–165 drivers), but demand is only gradually rising:

14:00 & 15:00: 71 requests vs 125–139 drivers

17:00: 98 requests vs 180 drivers

🔎 Insight: Extended oversupply period during mid-day. Driver earnings may suffer due to low ride frequency.

4. 🌆 Evening Peak (18:00–22:00)
Demand and supply both peak, indicating solid performance:

18:00: 119 requests vs 174 drivers

19:00: 156 requests vs 180 drivers

22:00: 174 requests vs 144 drivers

🔎 Insight: High demand aligns well with supply till 9 PM. A slight driver shortfall at 10 PM may cause longer wait times or missed trips.

5. 🌙 Late Night (23:00)
184 requests vs 119 drivers

🔥 Insight: High demand and under-supply — one of the biggest gaps. This hour is a critical opportunity zone.

