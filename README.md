# Copper Integration

## Overview

The provided sample includes:

- Connecting to the Copper API
- Interacting with the following objects:
  - Users
  - People
  - Opportunities

### Additional resources

- <https://app.prosperworks.com/companies/391648/app#/settings/api-keys>

- <https://developer.copper.com/index.html>

- <https://support.copper.com/hc/en-us/articles/115000816826-Code-samples-and-tips>

---

## Dependencies
#### *Linx Designer*
This solution was developed in the Linx Designer v5.20.2.0
#### *Copper API*
The version of the Copper API at the time of writing is 2021-05.

### Pre-requisites

- Linx Designer
- Copper account

---

## Setting up the sample

1. Create a new account on Copper
1. You'll need your API Key from Copper to enter into the API Endpoint URL. To generate an API Key, in the Copper web app go to System settings > API Keys and click the GENERATE API KEY button.

Note the **API Key** and **Email (Creator)** details.

Open and Configure the Solution's $.Settings:

1. Open the solution in your Linx Designer.
1. Edit the $.Setting values:
   1. ApiToken: Your **API Key**.
   1. Email : Your Email
1. Save the Solution.
---

## Using the sample

---

Generic Templates
Description: The templates can be used as follows:

Opportunities:
1. ListOpportunities_SearchBy
Usage:
  - Parameter: Receives a JSON string for CallRESTEndpoint body 
  - Result: Receives Opportunity List 

2. ListPipelines
Usage:
  - Result: Receives Pipelines List 

People:
1. CreateNewPerson
Usage:
  - Parameter: Receives a JSON string for CallRESTEndpoint body 
  - Result: Receives person created as a JSON string

2. ListPeople_SearchBy
Usage:
  - Parameter: Receives a JSON string for CallRESTEndpoint body
  - Result: Receives People List 

3. UpdatePerson
Usage:
  - Parameter: Receives a JSON string from CallRESTEndpoint body
  - Result: Receives person updated as a JSON string 

Users:
1. ListUsers
Usage:
  - Result: Receives Users List 
Utilities
  - FormatDate
Usage:
Converts a unix timestamp to datetime

---
Running the samples
- Open and configure the settings. 
- Create a directory at ‘C:\Temp\Copper\’ , for $.Settings.LogFile and $.Settings.WorkSheetPath in Linx Designer. TextFile log.txt and Excel sheet Report.xlsx will be created in ‘C:\Temp\Copper\’.  You can always change the paths in the settings according to your choice.
 
**CreateANewPerson**
  - Creates a new person and saves the result in a log file in the path $.Settings.LogFile

**ListPipelines**
  - Get Pipelines and saves the data in the Excel sheet $.Settings.WorkSheetPath in Sheet 3.

**SaveOpenOpportunities_In_Excel**
  - Get Opportunities list and saves the data in the Excel sheet $.Settings.WorkSheetPath in Sheet 2.

**SavePeople_In_Excel**
  - Get people and saves the data in the Excel sheet $.Settings.WorkSheetPath in Sheet 1.

**UpdatePerson**
  - Updates person and saves response from $.Settings.LogFile
       - Before running the UpdatePerson, open the file created in $.Settings.LogFile from CreateANewPerson.  Copy the id from the textfile 

- Go to Samples>UpdatePerson 
- Click on the Function UpdatePerson in the designer
- In the properties window, in the parameters section, locate id and paste the id copied from the textfile above.


