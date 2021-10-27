# Webscraping_Project
Data-oriented job market analysis utilising webscraped data from Glassdoor HK.
This is my first project using Python for data analysis, we chose to webscraped data from Glassdoor HK to understand more about data-oriented roles in the job market of Hong Kong.

## Our Goal
To increase transparency and clarify data-oriented job market in Hong Kong.

## Business Value
- To offer a solution on how to optimise job search for prospective Data Analysts / Data Engineers / Data Scientists.
- To provide corporate HRs / recruiting firms with an efficient way of conducting competitive measurement (quant vs qual).

## Data Collection
Webscraped multiple pages of job postings from Glassdoor HK for the following roles:
- Data Analyst
- Data Engineer
- Data Scientist

## Data Preprocessing
1. Scraped Glassdoor for each role using Selenium; Data processing with Pandas, Time, Numpy, OS, Math, Regex
<img width="683" alt="Screenshot 2021-10-27 at 8 34 03 AM" src="https://user-images.githubusercontent.com/84705479/138980436-f05d61a7-b4f5-4ef4-aa3c-d0f54b5be8c6.png">
2. Merging & Cleaning
  - Merge 3 data frames (DA, DE & DS) together
  - Drop any duplicate rows
  - Drop any entries without company names to ensure high-quality data
  - Drop unnecessary columns
  - Ensure overall_score is extracted from the “employerStats” column
  - New column to categorise each role to
    (1) Data Analyst
    (2) Data Engineer
    (3) Data Scientist
<img width="732" alt="Screenshot 2021-10-27 at 8 36 39 AM" src="https://user-images.githubusercontent.com/84705479/138980592-75324995-ef2c-4bc2-b420-d973afc5352d.png">
<img width="705" alt="Screenshot 2021-10-27 at 8 39 00 AM" src="https://user-images.githubusercontent.com/84705479/138980726-25239ff4-ee5e-4d20-b287-95c410fbdf91.png">
