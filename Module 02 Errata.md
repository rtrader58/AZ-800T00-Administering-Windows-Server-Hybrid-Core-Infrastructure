# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 2 Errata

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell. <br>

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  

Step 9: If challenged with “Help us prove you’re not a bot” enter the Captia and hit submit. <br> 

### Exercise 1:  Preparing Azure AD for AD DS integration  

Task 1: Create a custom domain in Azure <br>
Step 2: Use the credential provided in the lab <br>

Task 2: Create a user with the Global Administrator role <br> 
Step 2: After selecting New Users, select Creat new user <br> 
Step 5: Click Next: Properties - Scroll sown to setting and set usage location as United States <br> 

After step 8, click on the new user you created and copy the new users User Principle Name.  I recommend you open Notepad on your computer connecting to the lab environment and paste the account so you can use it in future labs. <br> 

Task 3: Change the password for the user with the Global Administrator role  <br><br>
Step 3 and 4 :  Paste the logon name and passowrd you previously copied. <br> 
Step 5:  I pasted the password used by the labuser account found under the Resources tab <br>

Exercise 2: Preparing on-premises AD DS for Microsoft Entra ID integration <br>
Task 1: Install IdFix <br>
Step 1:  On SEA-ADM1, open Microsoft Edge, and then browse to +++https://github.com/microsoft/idfix+++ remove the +++ <br>

### Exercise 4: Verifying integration between AD DS and Azure AD  

Synchronization may take up to 15 minutes until the step 2 updates with status of synchronization.  <br>

### Exercise 5: Implementing Azure AD integration features in AD DS  

## Unable to do remaining steps in Task 1 due to Microsoft change to Licensing of Premium plans - Skip to Task 2

Task 5: Install and register the Azure AD Password Protection proxy service and DC agent - You can install but will be unable to register <BR>
Skip Task 6: Enable password protection in Azure <br>
Ensure you do Exercise 6: Cleaning up <BR>

