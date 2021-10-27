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
    - (1) Data Analyst
    - (2) Data Engineer
    - (3) Data Scientist
<img width="732" alt="Screenshot 2021-10-27 at 8 36 39 AM" src="https://user-images.githubusercontent.com/84705479/138980592-75324995-ef2c-4bc2-b420-d973afc5352d.png">
<img width="705" alt="Screenshot 2021-10-27 at 8 39 00 AM" src="https://user-images.githubusercontent.com/84705479/138980726-25239ff4-ee5e-4d20-b287-95c410fbdf91.png">

3. Further Cleaning
  - “salary”
    - Separate into Lower Range and Upper Range
<img width="1109" alt="Screenshot 2021-10-27 at 8 48 53 AM" src="https://user-images.githubusercontent.com/84705479/138981616-df0de5f2-c336-45a1-91bb-24ad8b1b9049.png">
  - “EmpBasicInfo”: 
    - Split extracted strings
    - Create dictionary for each job posting
    - Build a temporal list for each intended independent variable
    - Append each list with extracted value from all created dictionaries
 <img width="668" alt="Screenshot 2021-10-27 at 8 50 02 AM" src="https://user-images.githubusercontent.com/84705479/138981634-91a95b5e-ea3d-4fdf-a1e2-3e513c5f1aec.png">
<img width="1056" alt="Screenshot 2021-10-27 at 8 50 54 AM" src="https://user-images.githubusercontent.com/84705479/138981677-454468e1-fb0b-4650-9844-8c4f48ebc481.png">
4. Final Dataframe
<img width="895" alt="Screenshot 2021-10-27 at 8 51 34 AM" src="https://user-images.githubusercontent.com/84705479/138981732-18d5abd8-565f-4101-ad9a-a57970edb1d9.png">
