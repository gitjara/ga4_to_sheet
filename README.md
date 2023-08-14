# GA4 to Google Sheets

This program allows you to automatically fetch data from Google Analytics 4 (GA4) and upload it to Google Sheets.

## Table of Contents

- [Overview](#overview)
- [Setup](#setup)
  - [Prerequisites](#prerequisites)
  - [Configuration](#configuration)
- [Usage](#usage)
- [Getting a Google Service Account File](#getting-a-google-service-account-file)
- [Choosing Dimensions and Metrics](#choosing-dimensions-and-metrics)
- [License](#license)
## Overview

This program uses the Google Analytics Data API and gspread to interact with Google Sheets.
## Setup
### Prerequisites

1. Ensure you have a Google service account credential and that this service has been granted access to your Google Analytics 4 account and your Google Sheet.
2. Make sure you have the required packages installed:
   ```bash
   pip install google-analytics-data gspread oauth2client requests

### Configuration

Replace 'PATH to your Service acc file' with the path to your Google service account credential file.
Replace 'Your google sheet doc id' with the ID of your Google Sheets document.
Replace 'Your sheet name' with the name of the sheet you want to upload the data to.
Replace 'your property id' with your GA4 property ID.
## Usage

After setting up and configuring:

```bash
python path_to_script.py

The data will automatically be fetched from your GA4 account and uploaded to your Google Sheet.

## Getting a Google Service Account File

To get a Google service account file:

1. Go to the Google Cloud Console.
2. Create a new project or select an existing project.
3. Navigate to IAM & Admin > Service accounts.
4. Click on Create Service Account.
5. Fill in the details and click Create.
6. On the next page, grant necessary permissions to the service account (e.g., Google Analytics Data API access).
7. On the last step, click on Create Key and choose JSON format.
8. Your browser will download the JSON service account key.
9. Remember to share your Google Sheet with the email address associated with your service account (found in the JSON file under "client_email").
## Choosing Dimensions and Metrics

To choose the right dimensions and metrics for your GA4 report, use the GA4 Dimensions & Metrics Explorer. This tool helps you find the available dimensions and metrics that you can use to fetch data from GA4.
## License

This project is distributed under the MIT license. You can use, modify, and distribute it under the terms of this license.
