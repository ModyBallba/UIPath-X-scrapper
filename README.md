# Twitter Analytics Automation with UiPath

This UiPath project automates the process of scraping data from the Twitter (X) page `@Almosahf` using the Twitter API. The workflow extracts key metrics, performs calculations, and saves the data into CSV and Excel files. Additionally, it captures a screenshot of the latest tweet and handles various login scenarios. The process is designed to run every 24 hours using UiPath Orchestrator (though Orchestrator setup is not included as it is not free).

---

## Features

- **Twitter API Integration**: Fetches data from the `@Almosahf` Twitter page using the Twitter API.
- **Data Extraction**: Retrieves metrics such as:
  - Date
  - Followers
  - New Followers
  - Tweets Count
  - Tweets Today
  - Growth Rate (%)
  - Average Tweets/Day
- **Data Calculation**: Computes additional metrics like:
  - Followers Increase Goal
  - Avg Tweets Goal / Day
  - Enhanced Engagement Rates
- **Data Storage**: Saves the extracted and calculated data into:
  - A CSV file for raw data.
  - An Excel file for processed data.
- **Screenshot Capture**: Opens the `@Almosahf` Twitter page, handles login scenarios, and captures a screenshot of the latest tweet.
- **Scheduled Execution**: Designed to run every 24 hours (requires UiPath Orchestrator for scheduling, which is not included in this project).

---

## Prerequisites

1. **Twitter Developer Account**: Create a developer account on [Twitter Developer](https://developer.twitter.com/) and generate a Bearer Token for API access.
2. **UiPath Studio**: Ensure you have UiPath Studio installed to run the workflow.
3. **PDF OCR Activity**: Install the "PDF OCR" activity package in UiPath Studio for processing PDF data.
4. **Excel and CSV Libraries**: Ensure the necessary libraries for Excel and CSV handling are installed in UiPath.

---

## Setup Instructions

1. **Clone the Repository**: Clone this repository to your local machine.
2. **Add Bearer Token**:
   - Open the workflow in UiPath Studio.
   - Locate the HTTP Request activity where the Twitter API is called.
   - Replace the placeholder with your Bearer Token.
3. **Configure File Paths**:
   - Update the file paths for saving the CSV and Excel files in the workflow.
4. **Run the Workflow**:
   - Execute the workflow in UiPath Studio to test the functionality.
5. **Schedule the Workflow** (Optional):
   - Use UiPath Orchestrator to schedule the workflow to run every 24 hours (not included in this project).

---

## Workflow Steps

1. **Fetch Data from Twitter API**:
   - Use the Bearer Token to authenticate and retrieve data from the `@Almosahf` Twitter page.
2. **Calculate Metrics**:
   - Compute metrics such as Growth Rate, Average Tweets/Day, and engagement goals.
3. **Save Data**:
   - Save the raw data in a CSV file.
   - Save the processed data in an Excel file.
4. **Capture Screenshot**:
   - Open the `@Almosahf` Twitter page, handle login scenarios, and capture a screenshot of the latest tweet.
5. **Repeat Every 24 Hours**:
   - The workflow is designed to run daily (requires Orchestrator for scheduling).

---

## Output Files

1. **Raw Data CSV**:
   - Contains columns: `Date`, `Followers`, `New Followers`, `Tweets Count`, `Tweets Today`, `Growth Rate (%)`, `Average Tweets/Day`.
2. **Processed Data Excel**:
   - Contains calculated metrics: `Followers Increase Goal`, `Avg Tweets Goal / Day`, `Enhanced Engagement Rates`.
3. **Screenshot**:
   - A screenshot of the latest tweet from the `@Almosahf` Twitter page.

---

## Notes

- **Orchestrator Dependency**: Scheduling the workflow to run every 24 hours requires UiPath Orchestrator, which is not included in this project.
- **API Rate Limits**: Be mindful of Twitter API rate limits when running the workflow frequently.
- **Error Handling**: The workflow includes basic error handling for login scenarios and API failures.

---


## Contributions

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

---


