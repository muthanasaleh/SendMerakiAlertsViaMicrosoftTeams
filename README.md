# SendMerakiAlertsViaMicrosoftTeams
[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/muthanasaleh/SendMerakiAlertsViaSkype)

This is part of a project to have one Alert system for all network devices (Meraki Devices) in an organization. The main purpose of this application is to Check Meraki devices status in real time and sending text messages to a microsoft teams channel when a device's status is changed (Online/Offline).

## Requirements
 **To use this application you need:**
 
    - Python 3.7+
    - Meraki API key
    - An incoming webhook to a Teams channel
    - Python libraries: pymsteams and meraki

The application scans all devices within an organization and store the status of each device in a dictionary (for example {“Device1, offline”}). Then it loops through the list of all devices stored in the dictionary and send an alert if any device is offline to a microsoft teams channel (Your system admin MS teams account). The script runs every 2 minutes and it can be changed based on how critical the impact is on your business. However, running high-volume API monitoring tasks in realtime can over throttle the system and lead to 429 errors (Read More https://developer.cisco.com/meraki/api-v1/#!rate-limit)

## Install and Setup
1. Create a webhook in MS Teams

   - Add an incoming webhook to a Teams channel:

     Navigate to the channel where you want to add the webhook and select (•••) More Options from the top navigation bar.
     Choose Connectors from the drop-down menu and search for Incoming Webhook.
     Select the Configure button, provide a name, and optionally, upload an image avatar for your webhook.
     The dialog window will present a unique URL that will map to the channel. Make sure that you copy and save the URL — you will need to provide it to the outside service.
     Select the Done button. The webhook will be available in the team channel.
        
2. Install required libraries on Python
  - Meraki (https://pypi.org/project/meraki/)
    - pip install meraki
  - pymsteams
    - pip install pymsteams(https://pypi.org/project/pymsteams/)
  - [Learn more about pip command](https://pip.pypa.io/en/stable/installation/)
  
3. Meraki API Key (https://documentation.meraki.com/General_Administration/Other_Topics/Cisco_Meraki_Dashboard_API)

## Using the application
  1. Download SendMerakiAlertsViaMicrosoftTeams.py
  2. Open the application with your Python IDLE https://www.python.org/downloads/
  3.	Edit Meraki API key value
  4.	Edit Organization ID value(How to get organization ID https://developer.cisco.com/meraki/api/#!get-organizations)
  5.	Create incoming Webhook (https://docs.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook)
  6.	Run the application

## Technologies used
  **The following technologies were used as part of this demo:**

  -	Cisco Meraki MX devices
  -	Cisco Meraki MS Devices
  -	Cisco Meraki MR devices
  -	Microsoft Microsoft Teams

## License
- Distributed under the MIT License. See LICENSE.txt for more information.
