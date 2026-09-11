# Setup using Qlik WebConnectors Package

You are on this page because you cannot use the built-in SMTP Connection by Qlik Sense itself, but go via the extra piece of software called "Qlik WebConnectors"

## Qlik WebConnectors Setup

Assuming that you have installed Qlik WebConnector Package from https://qlik-downloads.vercel.app or the official Qlik Download page. By default, it will be http on a port 5555

Go to the console of Qlik Web Connectors (http://localhost:5555/web/connector/SMTPConnector) 

  - Provide the following parameters
<img width="1500" height="966" alt="image" src="https://github.com/user-attachments/assets/d2dad297-7acc-48ff-a2bc-a2ca8d4e9e27" />

 - Then scroll down and click the green "Save Inputs & Run Table" button. 
 - Fix settings of SMTP and user until you get a working result:

<img width="667" height="198" alt="image" src="https://github.com/user-attachments/assets/c61543fb-0648-4203-a688-3de497d69302" />

 - Grab the loadAccessToken from the "Qlik Sense (Standard Mode)" tab: copy the code, we will need it in the REST Data Connection setup next

<img width="1895" height="906" alt="image" src="https://github.com/user-attachments/assets/71344fc1-f5cf-4ca6-b313-63f53ae6ce00" />

## Setup a REST Data Connection in Qlik Sense

Create a data connection of type REST. This is to communicate with the Qlik WebConnector Service, which wraps the SMTP sending of the mail.

We tell every parameter via a Query Parameter, so below is a long list of what you need to provide to work. 

Four parameters will later be set by the load script, so they have only temporary character during the creation of the data connection. However most parameters are taken for all the messages being sent, they act as a general default

<img width="630" height="755" alt="image" src="https://github.com/user-attachments/assets/df0f016e-d0d7-4b98-8cf0-8ba7d7631481" />

 
| Query Parameter	| Value |	Comment |	Set by script |
|-|-|-|-|
|connectorID|SMTPConnector|fix||	 
|table|SendEmail|fix||	 
|SMTPServer|your.server.com|change if needed||	 
|Port|25|change if needed	 ||
|SSLmode|None|change if needed||	 
|to|test.recipient@company.com|test during setup|X|
|cc||test during setup|X|
|subject|Test from Qlik Sense Data Connection|test during setup|X|
|message|Sent while editing Data Connection|test during setup|X|
|html|True|fix||	 
|fromName|Qlik Sense|change if needed	||
|fromEmail|r25p.bi@wienerlinien.at|change if needed	||
|delayInSeconds|0|fix||	 
|ignoreProxy|False|change if needed	 ||
|format|csv|fix||	 
|loadAccessToken|1h7jh3i6h3o7k|copy from previous setup	 ||
|UserName|smtp.user|change if needed||
|Password|smtp_user_password|change if needed||

**Note** you must enable "allow WITH CONNECTION" 



