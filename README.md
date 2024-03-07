Google sheet link https://docs.google.com/spreadsheets/d/1-GhV-tLSEsO02qnRDObQZHGwss8ggxWtPVHJ3R8yS2Q/edit#gid=0
Project Setup Instructions:
Clone Repository:
bash
Copy code
git clone <repository_url>
Install Dependencies:
bash
Copy code
cd project_directory
npm install
How to Run the Project Locally:
Environment Variables:

Create a .env file in the project root directory.
Add the following environment variables:
makefile
Copy code
GOOGLE_SHEETS_CLIENT_EMAIL=<your_google_sheets_client_email>
GOOGLE_SHEETS_PRIVATE_KEY=<your_google_sheets_private_key>
Replace <your_google_sheets_client_email> and <your_google_sheets_private_key> with your Google Sheets service account credentials.

Run the Project:

sql
Copy code
npm start
Open your web browser and navigate to http://localhost:3000 to view the project.

Details on the Google Sheets Integration:
The project integrates with Google Sheets for data storage. It uses the Google Sheets API to read and write data to a specific Google Sheet.

Integration Steps:
Set Up Google Sheets API:

Go to the Google Developers Console.
Create a new project and enable the Google Sheets API.
Create credentials for a service account.
Download the JSON key file for the service account.
Grant Access to Google Sheet:

Share the target Google Sheet with the email address associated with the service account.
Environment Variables:

Use the service account email and private key obtained from the JSON key file as environment variables (GOOGLE_SHEETS_CLIENT_EMAIL and GOOGLE_SHEETS_PRIVATE_KEY).
Read/Write Operations:

Use the Google Sheets API to read and write data to the specified Google Sheet.
Additional Features or Customizations Implemented:
User Authentication: Implemented user authentication using OAuth2.0 to restrict access to certain functionalities.
Real-time Updates: Integrated WebSocket for real-time updates when data changes in the Google Sheet.
Data Validation: Added validation checks to ensure data integrity before writing to the Google Sheet.
Error Handling: Implemented robust error handling to gracefully handle API errors and connectivity issues.
Logging: Utilized logging mechanisms to track user activities and system events for debugging and monitoring purposes.
