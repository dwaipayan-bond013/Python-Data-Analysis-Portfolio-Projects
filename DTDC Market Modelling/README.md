# 📦 DTDC Delivery Data Analysis
<p align="center">
  <img src="DTDC_Logo.jpg" width="1000px">
</p>

Welcome to the **DTDC Delivery Performance Analysis** project! This repository contains a comprehensive data analysis pipeline built in Python to evaluate and optimize the delivery network of DTDC, one of India's leading logistics companies.

## Project Description

In this project, we dive deep into delivery trip data to uncover hidden inefficiencies, regional logistics trends, and route-level performance metrics. Our goal is to help stakeholders make data-driven decisions to improve delivery accuracy, reduce delays, and boost customer satisfaction.

We work with a dataset comprising **144,867+ delivery records**, including information on trip times, source-destination pairs, route types, estimated vs actual distances, and delays.

---

## Dataset Highlights

### Column Description:-

#### • data - tells whether the data is testing or training data
#### • trip_creation_time – Timestamp of trip creation
#### • route_schedule_uuid – Unique Id for a particular route schedule
#### • route_type – Transportation type
#### • FTL – Full Truck Load: FTL shipments get to the destination sooner, as the truck is making no other pickups or drop-offs along the way
#### • Carting: Handling system consisting of small vehicles (carts)
#### • trip_uuid - Unique ID given to a particular trip (A trip may include different source and destination centers)
#### • source_center - Source ID of trip origin
#### • source_name - Source Name of trip origin
#### • destination_cente – Destination ID
#### • destination_name – Destination Name
#### • od_start_time – Trip start time
#### • od_end_time – Trip end time
#### • start_scan_to_end_scan – Time taken to deliver from source to destination
#### • is_cutoff – Unknown field
#### • cutoff_factor – Unknown field
#### • cutoff_timestamp – Unknown field
#### • actual_distance_to_destination – Distance in Kms between source and destination warehouse
#### • actual_time – Actual time taken to complete the delivery (Cumulative)
#### • osrm_time – An open-source routing engine time calculator which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) and gives the time (Cumulative)
#### • osrm_distance – An open-source routing engine which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) (Cumulative)
#### • factor – Unknown field
#### • segment_actual_time – This is a segment time. Time taken by the subset of the package delivery
#### • segment_osrm_time – This is the OSRM segment time. Time taken by the subset of the package delivery
#### • segment_osrm_distance – This is the OSRM distance. Distance covered by subset of the package delivery
#### • segment_factor – Unknown field

## 🎯 Key Objectives

- Explore patterns in delivery delays and identify high-risk routes.
- Compare actual vs OSRM (Open Source Routing Machine) estimates for time and distance using EDA and A/B testing.
- Analyze transport mode effectiveness (Carting vs FTL).
- Uncover regional trends in delivery traffic.
- Provide actionable recommendations to improve route efficiency.

---

## Technologies Used

- **Python 3.x**
- **Pandas, NumPy** – Data manipulation
- **Matplotlib, Seaborn** – Data visualization
- **Jupyter Notebook** – Exploratory analysis and documentation

---


---

## 📊 Visual Insights

Key insights are visualized through bar plots, box plots, heatmaps, and scatter plots to simplify interpretation and storytelling.

---

## 📌 Outcomes

- Identified top 5 high-volume delivery states and cities
- Found that actual deliveries take **27% longer** on average than OSRM estimates
- Determined **FTL is more time-efficient** compared to Carting
- Highlighted critical city-pairs and underperforming segments

---

## 🧠 Conclusion

This analysis serves as a foundation for improving DTDC’s logistics operations using historical data and smart visual analytics. It can be extended to support real-time routing systems or SLA compliance monitoring frameworks.

---

## 🚀 Getting Started

To run the notebook:

1. Clone the repository
2. Install dependencies from `requirements.txt`
3. Launch the notebook with Jupyter or VS Code
4. Explore insights and modify visualizations as needed

---

## 📬 Contact

For questions or collaboration inquiries, feel free to reach out via [LinkedIn](https://linkedin.com) or open an issue in this repo.


