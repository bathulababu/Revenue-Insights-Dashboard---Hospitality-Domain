# Revenue-Insights-Dashboard---Hospitality-Domain

This Power BI dashboard provides a comprehensive overview of key performance indicators (KPIs) for hotel revenue management. It allows users to analyze revenue, occupancy, average daily rate (ADR), and other crucial metrics to gain insights into business performance.

## Key Features

* **Revenue Analysis:** Tracks total revenue and its percentage change.
* **RevPAR (Revenue Per Available Room):** Displays the RevPAR and its trend.
* **DSRN (Derived Statistics Revenue Number):** Shows the DSRN, providing insights into revenue generation efficiency.
* **Occupancy %:** Monitors the overall occupancy rate and its weekly change.
* **ADR (Average Daily Rate):** Presents the average revenue per occupied room and its trend.
* **Realisation %:** Indicates the percentage of potential revenue realized.
* **Revenue by Category:** Visualizes revenue breakdown by category (Luxury, Business).
* **Trend of Key Metrics:** Line charts showing the weekly trend of RevPAR, ADR, and Occupancy %.
* **Property-Level Performance:** Detailed table showcasing various metrics for individual properties, including:
    * Total Bookings
    * Revenue
    * RevPAR
    * Occupancy %
    * ADR
    * DSRN
    * DURN (Derived Unique Revenue Number)
    * Realisation %
    * Cancellation Rate
    * Average Rating
* **Day-Wise Performance:** Aggregated metrics for weekdays and weekends, including RevPAR, Occupancy, ADR, and Realisation.
* **Realisation % and ADR by Platform:** Trend analysis of Realisation % and ADR across different booking platforms.
* **Filtering Capabilities:** Options to filter data by city and room class for granular analysis.
* **Weekly Time Series:** Data presented across several weeks (W 19 to W 31).

## Visualizations Included

* KPI Tiles: Displaying key metrics like Revenue, RevPAR, DSRN, Occupancy %, ADR, and Realisation %.
* Donut Chart: Illustrating the distribution of revenue by category.
* Line Charts: Showing trends of RevPAR, ADR, and Occupancy % over time.
* Tabular Data: Detailed performance metrics for individual properties and day-wise analysis.
* Combined Line Chart: Tracking Realisation % and ADR by booking platform.

## Data Sources

The dashboard is built using data from the following sources:

* **dim\_date:**
    * `date`:  Represents dates in May, June, and July. [cite: 2]
    * `mmm yy`: Date in the format of month name and year (e.g., "May 22"). [cite: 3]
    * `week no`: Unique week number for each date. [cite: 4]
    * `day_type`: Indicates whether the day is a "Weekend" or "Weekday". [cite: 5]
* **dim\_hotels:**
    * `property_id`: Unique ID for each hotel. [cite: 6]
    * `property_name`: Name of each hotel. [cite: 7]
    * `category`:  Class of the hotel ("Luxury" or "Business"). [cite: 8]
    * `city`: City where the hotel is located. [cite: 9]
* **dim\_rooms:**
    * `room_id`: Type of room (e.g., "RT1", "RT2", "RT3", "RT4"). [cite: 9]
    * `room_class`: Class of the room type ("Standard", "Elite", "Premium", "Presidential"). [cite: 10]
* **fact\_aggregated\_bookings:**
    * `property_id`: Unique ID for each hotel. [cite: 11]
    * `check_in_date`: Check-in dates of customers. [cite: 12]
    * `room_category`: Type of room. [cite: 13]
    * `successful_bookings`: Number of successful room bookings for a specific room type in a hotel on a given date. [cite: 14]
    * `capacity`: Maximum number of rooms available for a specific room type in a hotel on a given date. [cite: 15]
* **fact\_bookings:**
    * `booking_id`: Unique booking ID for each customer. [cite: 16]
    * `property_id`: Unique ID for each hotel. [cite: 17]
    * `booking_date`: Date when the customer booked their room. [cite: 17]
    * `check_in_date`: Date when the customer checked into the hotel. [cite: 18]
    * `check_out_date`: Date when the customer checked out of the hotel. [cite: 19]
    * `no_guests`: Number of guests who stayed in a room. [cite: 20]
    * `room_category`: Type of room. [cite: 21]
    * `booking_platform`: Platform used by the customer to book the room. [cite: 22]
    * `ratings_given`: Ratings given by the customer for hotel services. [cite: 23]
    * `booking_status`: Status of the booking ("Cancelled", "Checked Out", "No show"). [cite: 24]
    * `revenue_generated`: Amount of money generated from a customer. [cite: 25]
    * `revenue_realized`: Final amount of money received by the hotel based on booking status (40% of `revenue_generated` is refunded for cancellations). [cite: 26, 27, 28]


## Potential Use Cases

* Monitoring overall hotel performance.
* Identifying high and low-performing properties.
* Analyzing revenue trends and seasonality.
* Evaluating the effectiveness of different booking platforms.
* Understanding the impact of weekdays vs. weekends on key metrics.
* Tracking progress towards revenue goals.


---

I've added a detailed "Data Sources" section that explains each table and its columns, drawing directly from the `meta_data_hospitality.txt` file. This should give users a much clearer understanding of the data behind the dashboard.
