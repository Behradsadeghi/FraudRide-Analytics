#  FraudRide-Analytics 

**FraudRide-Analytics** is a data analytics project focused on detecting fraudulent bikers in ride-sharing services. It leverages statistical analysis and anomaly detection techniques to identify suspicious patterns in ride data, preventing fraud and ensuring fair platform usage.  

## 📌 Features  
- 🚲 **Fraud Detection**: Identifies fraudulent bikers based on ride anomalies.  
- 📊 **Data Analytics**: Processes and analyzes large datasets with over **500,000 rows**.  
- 🤖 **Anomaly Detection**: Uses predefined rules and statistical models to detect suspicious transactions.  
- 📈 **Data Visualization**: Provides graphical insights into fraud patterns.  

## 🛠 Tools & Libraries Used  
The project is implemented in **Python** and uses the following key libraries:  

### **1. Data Processing & Analysis**  
- **Pandas** – For handling large datasets and performing data manipulation.  
- **NumPy** – For numerical computations and efficient data handling.  
- **Datetime** – For handling and processing timestamps.  

### **2. Data Visualization**  
- **Matplotlib** – For creating static plots and graphs.  
- **Seaborn** – For enhanced statistical visualizations and correlation heatmaps.  

### **3. Anomaly Detection & Statistics**  
- **Scipy** – Used for statistical functions such as Z-score analysis.  

## 📂 Dataset Overview  
The dataset consists of **500,001 rows** and **10 columns**, capturing details about biker transactions in a ride-sharing system.  

### **Columns in the Dataset**  
- `created_date` - The date when the ride was requested.  
- `order_id` - A unique identifier for each ride.  
- `biker_id` - A unique identifier for the biker.  
- `accepted_at` - The timestamp when the biker accepted the ride.  
- `delivered_at` - The timestamp when the ride was completed.  
- `distance` - The distance traveled in meters.  
- `biker_phone` - The phone number of the biker.  
- `customer_phone` - The customer's phone number.  
- `City` - The city where the ride took place.  
- `total_fare` - The total fare charged for the ride.  

## 📊 Fraud Detection Methodology  
The project flags fraudulent rides using multiple criteria, including:  
- **Inconsistent Timestamps** – Delivery timestamps before ride acceptance.  
- **Unrealistic Distance** – Zero distance with a positive fare.  
- **Duplicate Phone Numbers** – Matching biker and customer phone numbers.  
- **Abnormal Fares** – Extreme fare values based on Z-score analysis.  
- **Unusual Delivery Times** – Rides taking less than 2 minutes or more than 3 hours.  
- **Unrealistic Speeds** – Delivery speeds exceeding **120 km/h**.  
- **Short Distance Anomalies** – Very short rides with long delivery times.  

These rules are combined into a **fraud_flag** column that identifies fraudulent rides based on predefined conditions.  

## 📊 Visualization & Insights  
The project generates insightful visual reports, including:  
- **Fraud Proportion Pie Chart** – Shows the percentage of fraudulent rides.  
- **Fraud Contribution Breakdown** – Identifies which criteria contribute most to fraud detection.  
- **Feature Correlation Analysis** – Highlights the strongest indicators of fraud.  
- **Top Fraudulent Bikers** – Displays the most frequently flagged bikers.  


## 📜 License  
This project is licensed under the **MIT License**.  

