# SendMerakiAlertsViaMicrosoftTeams
How to monitor your Meraki devices status per organization and send alerts to your Microsoft teams account once the device status is changed (Online/Offline)
Requirement:
1. Create a webhook in MS Teams

    Add an incoming webhook to a Teams channel:

    Navigate to the channel where you want to add the webhook and select (•••) More Options from the top navigation bar.
    Choose Connectors from the drop-down menu and search for Incoming Webhook.
    Select the Configure button, provide a name, and optionally, upload an image avatar for your webhook.
    The dialog window will present a unique URL that will map to the channel. Make sure that you copy and save the URL — you will need to provide it to the outside service.
    Select the Done button. The webhook will be available in the team channel.

    more details can be found on https://docs.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook

2. Install pymsteams

    pip install pymsteams
