# City Temperature Automation

## Project Description
This UiPath automation reads city names from an Excel file, searches Google for current temperatures, and writes the temperatures back to the Excel file.

## How to Run
1. Open the project in UiPath Studio (Community Edition).  
2. Make sure the Excel file `citylist.xlsx` is in the project folder.  
3. Run the workflow `.xaml` file.  
4. The Excel file will be updated with temperatures in Column B.

## Prerequisites
- UiPath Studio Community Edition installed  
- Internet connection for Google search  
- Excel file with city names in Column A

## Notes
- The workflow includes error handling for missing or invalid city names.
- All UiPath activities are annotated for clarity.
## Test Plan

| Test Case | Description                                    | Expected Result                           |
|-----------|------------------------------------------------|------------------------------------------|
| 1         | Open Excel file with city names                 | Excel opens without errors                |
| 2         | For each city, Google search returns temperature | Temperature is displayed correctly on Google |
| 3         | Temperature is written back into Excel Column B | Column B shows correct temperatures       |
| 4         | Handle invalid or empty city names               | Automation skips invalid entries gracefully |

---

## List of Variables and Types

| Variable Name | Type         | Purpose                              |
|---------------|--------------|------------------------------------|
| cityNames     | List<String> | Stores city names read from Excel  |
| temperature   | String       | Holds the temperature retrieved from Google |
| currentRow    | Integer      | Tracks the current Excel row for reading/writing |
