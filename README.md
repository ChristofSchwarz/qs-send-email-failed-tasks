# qs-send-email-failed-tasks
Send Emails to app owners if a reload task fails.

The app can work in two ways
 - using Qlik Sense native's SMTP Connection
 - using Qlik Web Connector Package as wrapping service (and a REST connection to the connector)

The first option is recommended (no additional software needed), but some settings are not available - for example unauthenticated SMTP servers or using port 25.
The script variable `vSendMailConnectionType` decides which method to use.

Prerequisites
 - Setup and configure Qlik SMTP Connection

<img width="476" height="326" alt="image" src="https://github.com/user-attachments/assets/73f2e968-fd77-4b54-a722-542bbe37d9d4" />

 - access to system default data connection "monitor_apps_REST_user", "monitor_apps_REST_task" and "monitor_apps_REST_app"
 

Steps
 - upload .qvf file
 - edit script
     - page Main
     - vServerMainUrl to Qlik cluster's main url

 - Create a connection "SendMail"
