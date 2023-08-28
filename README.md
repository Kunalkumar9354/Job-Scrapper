# Job-Scrapper

Project Summary: Times Job Scraper

This project is an interactive script that scrapes job listings from the Times Jobs website based on user-provided skills and displays job details. It is designed to run indefinitely, periodically scraping jobs and waiting between iterations.

Main Components:

1. Imports:
   - The required libraries are imported, including `requests`, `BeautifulSoup`, `time`, and `Path` from the `pathlib` module.

2. ScrapeJobs Function:
   - The `ScrapeJobs` function is defined to perform the job scraping process.
   - It sends HTTP requests to the Times Jobs website and uses BeautifulSoup to parse the HTML content.
   - It interacts with the user to input unfamiliar skills.
   - It searches and extracts job details from the parsed HTML.
   - It filters jobs based on user-defined skills and stores the job details in text files within a "posts" directory.
   - This function is used for multiple iterations, ensuring fresh job scraping and waiting between iterations.

3. Main Execution:
   - The main execution block of the script is protected by the `if __name__ == "__main__":` condition.
   - The script runs in an infinite loop using a `while True` loop.
   - The `ScrapeJobs` function is repeatedly called to scrape jobs and store details.
   - A waiting time of 6 seconds is added between iterations to avoid overloading the website.

4. Adding Multiple Unfamiliar Skills:
   - The script is enhanced to allow users to input multiple unfamiliar skills separated by commas.
   - The input is split into a list of skills, and leading/trailing spaces are removed.
   - Jobs are filtered based on any unfamiliar skill's absence in the job's key skills.

Execution Flow:

1. Import required libraries.
2. Define the `ScrapeJobs` function for job scraping and filtering.
3. Execute the main block when the script is run directly.
   - Start an infinite loop.
   - Call the `ScrapeJobs` function.
   - Wait for 6 seconds before the next iteration.

Notes:

- The project demonstrates web scraping, user input, file handling, and the creation of a "posts" directory for storing job details.
- The script is built incrementally, adding features such as searching functionality and support for multiple unfamiliar skills.
