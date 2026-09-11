# Setup using Qlik WebConnectors Package

Go to the console of Qlik Web Connectors (http://localhost:5555/web/connector/SMTPConnector) 
  - Provide the following parameters

<img width="630" height="755" alt="image" src="https://github.com/user-attachments/assets/df0f016e-d0d7-4b98-8cf0-8ba7d7631481" />

 
| Query Parameter	| Value |	Comment |	Set by script |
|-|-|-|-|
|connectorID|SMTPConnector|fix||	 
|table|SendEmail|fix||	 
SMTPServer	wit-mx.wienit.at	change if needed	 
Port	25	change if needed	 
SSLmode	None	change if needed	 
to	Patel.DHRUVKUMAR.extern@wienerlinien.at	test during setup	X
cc	
test during setup	X
subject	Test from Qlik Sense Data Connection	test during setup	X
message	Sent while editing Data Connection	test during setup	X
html	True	fix	 
fromName	Qlik Sense	change if needed	 
fromEmail	r25p.bi@wienerlinien.at	change if needed	 
delayInSeconds	0	fix	 
ignoreProxy	False	change if needed	 
format	csv	fix	 
loadAccessToken	1h7jh3i6h3o7k	copy from previous setup	 
UserName	r25p.bi@wienerlinien.at	change if needed	 
Password	
change if needed	
(the current setup did not require a password
