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
  
  - “EmpBasicInfo” 
    - Split extracted strings
    - Create dictionary for each job posting
    - Build a temporal list for each intended independent variable
    - Append each list with extracted value from all created dictionaries
 <img width="668" alt="Screenshot 2021-10-27 at 8 50 02 AM" src="https://user-images.githubusercontent.com/84705479/138981634-91a95b5e-ea3d-4fdf-a1e2-3e513c5f1aec.png">
<img width="1056" alt="Screenshot 2021-10-27 at 8 50 54 AM" src="https://user-images.githubusercontent.com/84705479/138981677-454468e1-fb0b-4650-9844-8c4f48ebc481.png">

4. Final Dataframe
<img width="895" alt="Screenshot 2021-10-27 at 8 51 34 AM" src="https://user-images.githubusercontent.com/84705479/138981732-18d5abd8-565f-4101-ad9a-a57970edb1d9.png">

## Analysis - The Job Market
<img width="612" alt="Screenshot 2021-10-27 at 8 55 07 AM" src="https://user-images.githubusercontent.com/84705479/138982047-8d098f5c-7193-4dbb-863b-6a2ec1b8c2cc.png">
As of 20 June 2021, job postings were dominated by Data Engineer by an exceptionally large margin:

- 540 Data Engineers
- 308 Data Scientists
- 174 Data Analysts

<img width="608" alt="Screenshot 2021-10-27 at 8 55 18 AM" src="https://user-images.githubusercontent.com/84705479/138982124-d8401339-4ac6-4d58-8956-019299eb5392.png">
The following sectors lead the demand for data-oriented roles in terms of :

1. Business Services
2. Finance
3. Information Technology

Aside from the TOP 3 (>60%) above:
- Applying for Data Engineer roles? Be on the lookout for ones in Manufacturing.
- Prospective Data Scientists? Pay attention to the Retail sector.

<img width="533" alt="Screenshot 2021-10-27 at 8 55 28 AM" src="https://user-images.githubusercontent.com/84705479/138982228-984df5e1-3697-49e5-945f-19ae374d72e9.png">

Recruiter Galore!
- Data Analyst: Multiple industries already account for 10%+ of job postings, indicating that corporates are familiar with the scope of Data Analyst roles.
- Data Engineer / Data Scientist: Largely posted by Staffing & Outsourcing firms, representing ~15% and ~24% of such job posts.

<img width="582" alt="Screenshot 2021-10-27 at 8 55 36 AM" src="https://user-images.githubusercontent.com/84705479/138982603-54f80db0-1428-4295-aeec-43f0ca0dc771.png">

9 out of 10 of the companies are professional recruiting specialists.
Applying for Data Engineer / Data Scientist roles?
Be prepared to face the recruiters first!

## Analysis - Salary per size of companies
<img width="1160" alt="Screenshot 2021-10-27 at 9 05 33 AM" src="https://user-images.githubusercontent.com/84705479/138982796-918f378a-1aad-4336-a03a-8649a5402a7e.png">

## Analysis - Overall score per size of companies
<img width="1160" alt="Screenshot 2021-10-27 at 9 06 22 AM" src="https://user-images.githubusercontent.com/84705479/138982847-dd7d96fe-7aee-449a-9fe3-febe83c6c6be.png">
<img width="1157" alt="Screenshot 2021-10-27 at 9 06 46 AM" src="https://user-images.githubusercontent.com/84705479/138982874-c07632b5-44ab-4b4f-95ab-f941735d1cd4.png">
<img width="1137" alt="Screenshot 2021-10-27 at 9 07 27 AM" src="https://user-images.githubusercontent.com/84705479/138982946-a330c0e5-3d55-42c3-9621-146594e89b9c.png">

Salary won’t buy your employees’ happiness!

### Findings and suggestion in terms of company’s score & salary
Overall Score is the average of the scores below:
1. Compensation & Benefits
2. Culture & Values
3. Career Opportunities
4. Work/Life Balance
5. Senior Management

For middle-size companies:
- They pay the lowest salary and score the lowest overall score from employees
- Given no obvious correlation between salary and overall score, our suggestions for them in order to improve the above-mentioned factors to gain higher score from employees are:
  - Retain talents in the company
  - Reduce the turnover cost
