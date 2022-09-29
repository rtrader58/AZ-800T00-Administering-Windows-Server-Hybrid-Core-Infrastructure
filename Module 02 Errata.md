# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 2 Errata

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  <br>

Step 9: If challenged with “Help us prove you’re not a bot” enter the Captia and hit submit.  

### Exercise 1:  Preparing Azure AD for AD DS integration  

Task 1: Create a custom domain in Azure 
Step 2:  Use the credential used to redeem the Azure Pass  

Task 2: Create a user with the Global Administrator role  
After step 8, click on the new user you created and copy the new users User Principle Name.  I recommend you open Notepad on your computer connecting to the lab environment and paste the account so you can use it in future labs.  

Task 3: Change the password for the user with the Global Administrator role  
Step 3:  Paste the logon name you previously copied.  

### Exercise 4: Verifying integration between AD DS and Azure AD  

Synchronization may take up to 15 minutes until the step 2 updates with status of synchronization.  

### Exercise 5: Implementing Azure AD integration features in AD DS  

Task 1: Enable self-service password reset in Azure 
Step 12:  It may take up to 15 minutes before Password Reset is available after activating the P2 subscription.  Try refreshing the screen 

Task 5: Install and register the Azure AD Password Protection proxy service and DC agent <br> 
Steps 7, 8 and 9 the CMDlets need to be copied and pasted as individual commands.  If needed, when pasting the commands remove the >> at the end<br>
Step 7:  When pasting the 2nd and 3rd  line change the .msi to .exe <br>
Step 8: Wait approximately 5 minutes before running the restart command to allow the Agent to install 


 