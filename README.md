# Hotel Booking Demand: Why Do Guests Cancel?

## Project Overview
Cancellations are a major challenge for the hospitality industry-an empty room that was booked and canceled represents lost revenue. In this project, I analyze **119,390 bookings** from two hotels in Portugal (a City Hotel and a Resort Hotel) covering arrival dates from July 2015 to August 2017.

Drawing on my real-world experience working in a hotel, I combine exploratory data analysis with domain knowledge and statistical hypothesis testing to identify the main drivers of cancellations and provide actionable business recommendations.

## Dataset
The dataset used in this analysis is the **Hotel Booking Demand** dataset from [Kaggle](https://kaggle.com) (originally compiled by Antonio, Almeida, and Nunes, 2019).

## Key Findings
- **Overall Cancellation Rate:** **27.7%** of all cleaned bookings (86,637) were canceled, representing roughly **€11.5M (33.3%)** in estimated booked revenue. The City Hotel has a higher cancellation rate (**30.2%**) than the Resort Hotel (**23.7%**).
- **Lead Time Impact:** Cancellation risk rises sharply with lead time-from **8.5%** (0-7 days before arrival) to **39.9%** (180+ days in advance).
- **Booking Channels:** **Online Travel Agencies (Online TA)** generate 59% of all bookings and have the highest cancellation rate (**35.6%**), more than double that of **Direct** (**14.9%**) and **Corporate** (**12.2%**) bookings.
- **Guest Engagement & Loyalty:** Repeated guests cancel significantly less (**8.2%** vs. 28.4%), as do guests who make at least one special request (**21.8%** vs. 33.5%, especially in the City Hotel).
- **Pricing & Channel Hypothesis (Welch's t-test):** Controlling for hotel type, Online TA guests do **not** pay lower rates than Direct guests. In fact, Direct guests pay slightly more (+€2.6 to +€3.2 per night, *p* < 0.05).
- **Seasonality & Families:** The Resort Hotel relies heavily on summer dynamic pricing (ADR jumps from **€46 in January to €190 in August**). Bookings with children generate **+43% more revenue** per booking in the City Hotel and **+80% more** in the Resort Hotel.

## Visual Highlights

### 1. Lead Time & Cancellation Risk
![Lead Time and Cancellation Rate](lead_time_cancellations.png)

### 2. Seasonality: Guest Volume & Average Daily Rate (2016)
![Confirmed Guests and Average ADR by Month](monthly_guests_and_adr.png)

### 3. Revenue per Booking & Length of Stay
![Average Revenue and Length of Stay](revenue_and_stay_duration.png)


## Key Business Recommendations
- **Shift guests to Direct bookings with perks, not discounts:** Offer late check-out or a welcome drink on the hotel website to save agency commissions without lowering ADR.
- **Tighten rules for high-risk bookings:** Introduce partial prepayments or non-refundable rates for Online TA and Group bookings made 90+ days in advance.
- **Collect guest preferences after booking:** Send a short pre-arrival form (especially in the City Hotel), as guests with special requests cancel significantly less.
- **Target families and shoulder seasons:** Promote family packages in the Resort Hotel and run special offers in winter months (Jan–Feb, Nov–Dec) to boost occupancy.

## Tech Stack & Methods
- **Language:** Python 3
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Statistical Testing:** SciPy (Welch's t-test, Chi-square test of independence)
- **Environment:** VS Code (Jupyter Notebook extension)

## Repository Structure
- `hotel_bookings_analysis.ipynb` - Full analysis, visualizations, statistical tests, and business recommendations.
- `hotel_bookings.csv` - Dataset from Kaggle.

