
![project-logo](https://github.com/ajaym007/Pinterest-Pioneers_074/assets/172394805/2cdac22a-5f2a-413b-84b5-ba23d5563858)

STEPS OF DATA SCRAPPING FROM THE LINKEDIN WEBSITE

1. Setting Up:
    The code imports libraries to control a web browser and work with data.
    It stores your LinkedIn username and password.
    It sets up a tool to control the Chrome web browser.

2. Logging In:
    The code opens the LinkedIn website.
    It waits for the login page to load and then types your username and password.
    It clicks the login button and waits for the main LinkedIn page to load.

3. Preparing for Data Collection:
    The code creates a container to store job information (designation, company, etc.).
    It identifies all the page numbers on the current job listings page (assuming they have a specific class name).

4. Looping Through Job Listing Pages:
    The code loops through each page number, potentially scraping jobs from all available pages.
    On each page, it clicks the corresponding page number to navigate.
    It waits a few seconds (not ideal) to allow the page to load.
    The code then identifies all the job listings on the current page (assuming they have a specific class name).

5. Extracting Data from Each Job Listing:
    The code loops through each job listing on the current page.
    For each job listing, it clicks on it to open the details page.
    It scrolls down the page to the bottom.
    The code then tries to extract various details about the job and company from the page:

    Job title (designation)
    Company name
    Company size (number of employees)
    Company followers on LinkedIn
    Job seniority level
    Number of applicants (might be inaccurate)
    Job location!

      1. Job title (designation)
      2. Company name
      3. Company size (number of employees)
      4. Company followers on LinkedIn
      5. Job seniority level
      6. Number of applicants (might be inaccurate)
      7. Job location


6. Storing Extracted Data:
    If the code successfully finds each data element, it stores the information in the container created earlier.


Overall, this code automates logging into LinkedIn and scraping data from job listings across potentially multiple pages.

Here the code file link :codeforwebscraping.ipynb




[Dashboard 2](https://github.com/ajaym007/Pinterest-Pioneers_074/assets/103578366/b9936c86-bdcf-4ecb-8958-5b9126b79b21)



![er diagram final](https://github.com/ajaym007/Pinterest-Pioneers_074/assets/172352623/9dc12fbd-f836-422e-a6f3-508ae1df6477)


STEPS FOR DATA CLEANING : 

1. Concatenation of Data: Combined multiple CSV files into a single DataFrame using pandas' concat() function. This step ensured that all relevant data is consolidated into a single structure for uniform analysis.

2. Renaming Columns: Standardized column names to ensure consistency. For example, changed all column names to have the to respective requirement.

3. Creating Unique Identifiers: Generated unique values for job_id, company_id, and details_id columns to uniquely identify each job, company, and job details.

4. Converting 'LinkedIn Followers' to Numbers: Processed the 'LinkedIn Followers' column to extract numerical values and convert them to integers. This involved removing any non-numeric characters, such as commas and text, using string replacement and type conversion.

5. Processing 'Employee Count': Similar to the 'LinkedIn Followers' column, cleaned the 'Employee Count' column by removing non-numeric characters and converting the values to integers for consistent numerical analysis.

6. Extracting Strings from 'Total Applicants': Extracted the relevant numerical data from the 'Total Applicants' column, which contained strings with multiple pieces of information. This was achieved using regular expressions and string manipulation to isolate the number of applicants.

7. Cleaning the 'Industry' Column: Processed the 'Industry' column to extract only the industry name, removing any additional information like employee counts or other descriptors.

8. Standardizing the 'Level' Column: Cleaned the 'Level' column to standardize the job level descriptions. Extracted specific keywords like 'Full-Time', 'Internship', and 'Mid-Senior level', ensuring that only these relevant terms were retained.

9. Checking for Duplicates: Identified and removed any duplicate rows in the DataFrame to maintain data integrity and prevent redundancy.

10. Handling Missing Values: Checked for null values across all columns. Rows with missing values were removed to ensure completeness and reliability of the data.

11. Separating DataFrames: Separated the cleaned DataFrame into three distinct tables: jobs, company, and details. This was done based on the specific attributes relevant to each table.

12. Saving Cleaned Data to CSV: Saved the cleaned and separated DataFrames into individual CSV files for further analysis and usage. This ensured that each table (jobs, company, details) was stored in a structured format for easy access and analysis.




![Dashboard 2](https://github.com/ajaym007/Pinterest-Pioneers_074/assets/103578366/07358d0c-69d5-4721-bf8f-ff39f0612625)

