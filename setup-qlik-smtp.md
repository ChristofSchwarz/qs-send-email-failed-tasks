<img width="898" height="1600" alt="WhatsApp Image 2026-09-08 at 22 09 21" src="https://github.com/user-attachments/assets/abf303b5-de22-46bc-9629-989a8e936c88" /># Setup using Qlik Sense built-in SMTP Connection

 - Setup a new "Data Connection of type "SMTP Connection"

<img width="476" height="326" alt="image" src="https://github.com/user-attachments/assets/73f2e968-fd77-4b54-a722-542bbe37d9d4" />


 - edit script page Main
     - Set `vSendMailConnection` to the name of above new SMTP Connection
     - SET `vSendMailConnectionType` to 'REST'
     - vServerMainUrl to Qlik cluster's main url

