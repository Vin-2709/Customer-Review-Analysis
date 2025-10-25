#Customer-Review-Analysis

A simple dashboard-based system to analyse customer reviews and visualise insights.

🎯 Project Overview
This project implements a full data analytics pipeline, designed to transform raw customer feedback into an actionable, multi-page Power BI dashboard.

The core of this project is its advanced sentiment analysis engine. Instead of relying on simple positive/negative labels, this system uses a hybrid approach:

1.  VADER Sentiment Scoring: The Python script uses the NLTK VADER library to generate a quantitative `SentimentScore` for each raw review text.
2.  Nuanced Categorization: This score is then intelligently combined with the explicit star `Rating` provided by the user (e.g., 1-5 stars). This logic creates more granular and realistic categories like "Mixed Positive" (e.g., a 4-star review with slightly negative text) and "Mixed Negative" (e.g., a 3-star review with negative text).

This enriched data is then connected to social media and conversion metrics, presenting a complete business picture in an interactive dashboard with four main views:

Overview: A high-level summary of key performance indicators, including conversion rates, social media engagement, and the average customer sentiment rating.
Conversion Details: A drill-down into the customer journey funnel, showing how product conversion rates correlate with different customer actions.
Social Media: Visualizes social media engagement (Views, Clicks, Likes), allowing for analysis of content performance over time and by product.
Customer Review Details: The primary sentiment analysis view. This tab provides a detailed breakdown of review categories, correlates sentiment scores with user ratings in a scatter plot, and allows for drilling down to read the original feedback.

🧰 Tech Stack

Dashboard/Visualization: Power BI

Backend/Data Processing: Python (using pandas, pyodbc) and T-SQL (SQL Server)

Data Storage: SQL Server

Sentiment/Keyword Analysis: Python (using NLTK VADER)

📸 Dashboard Views
Overview 
<img width="1378" height="912" alt="Screenshot 2025-10-25 141418" src="https://github.com/user-attachments/assets/9cd8f39e-4c8d-4b5a-b330-ab872526c86b" />

A snapshot of high-level metrics across all data.

Conversion

<img width="1374" height="908" alt="Screenshot 2025-10-25 141447" src="https://github.com/user-attachments/assets/bbd8fbff-dc72-4e17-8a72-ccfcfe2a5e58" />

Shows how review sentiments correlate with conversions or other key business outcomes.

Social Media

<img width="1406" height="912" alt="Screenshot 2025-10-25 141503" src="https://github.com/user-attachments/assets/e370b2c9-7698-4e9e-9aed-25eadef5b1a3" />

Visualises social media mentions, engagement, sentiment trends over time.

Customer Review Details

<img width="1419" height="900" alt="Screenshot 2025-10-25 141515" src="https://github.com/user-attachments/assets/7037bda8-3902-4e33-881c-b66cc5f655a4" />

Detailed breakdown of reviews — sentiment, keywords, filtering, drilling down into individual feedback.

✅ Key Features

Ingests customer review data from multiple sources.

Performs sentiment analysis & extracts trending keywords.

Generates visual dashboards for quick insights.

Enables drill-down into detailed reviews for deeper analysis.

Connects sentiment trends to conversion/business metrics.

🚀 How to Set Up & Run

Clone the repository:

git clone https://github.com/Vin-2709/Customer-Review-Analysis.git
cd Customer-Review-Analysis


Install dependencies:

# Example for Node.js  
npm install  


or

# Example for Python backend  
pip install -r requirements.txt  


Configure any required environment variables/settings (e.g., API keys, database credentials).

Start the application:

# For frontend  
npm start  

# For backend (if applicable)  
python app.py  


Navigate to http://localhost:3000 (or whichever port) to view the dashboard.

📂 Folder Structure
Customer-Review-Analysis/
│
├── frontend/             # React (or other) dashboard code  
├── backend/              # Data processing & API code  
├── assets/               # Images, icons, etc.  
│   ├── overview.png  
│   ├── conversion.png  
│   ├── social_media.png  
│   └── customer_review_details.png  
├── data/                 # Raw & processed review data  
└── README.md             # This file  


