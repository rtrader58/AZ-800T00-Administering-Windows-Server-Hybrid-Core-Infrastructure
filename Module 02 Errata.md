# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 2 Errata

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up because they finish starting before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>

Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PowerShell. <br>

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  

Ignore the note you will be able to create a tenant <br>
Step 4: Type Microsoft Entra ID and Select <br>
Step 9: If challenged with “Help us prove you’re not a bot” enter the Captia and hit submit. <br> 

### Exercise 1:  Preparing Azure AD for AD DS integration  

Skip lab setup as you have already completed <br>
Task 1: Create a custom domain in Azure <br>
Step 2: Use the credential provided in the lab <br>

Task 2: Create a user with the Global Administrator role <br> 
Step 2: After selecting New Users, select Creat new user <br> 
After step 4: Copy the new users User Principle Name and Password into Notepad so you can use it in later steps <br>
Step 5: Click Next: Properties - Scroll sown to setting and set usage location as United States <br> 

Task 3: Change the password for the user with the Global Administrator role  <br>
Step 1: Open a New InPrivate window<br>
Step 3 and 4: Paste the logon name and password you previously copied. <br> 
Step 5:  I pasted the password used by the labuser account found under the Resources tab <br>
After Step 5: Close the New InPrivate window

### Exercise 2: Preparing on-premises AD DS for Microsoft Entra ID integration <br>

Task 1: Install IdFix <br>
Step 1: On SEA-ADM1, open Microsoft Edge, and then browse to +++https://github.com/microsoft/idfix+++ remove the +++ <br>

### Exercise 3: Downloading, installing, and configuring Microsoft Entra Connect

Ensure you are in the custom tenant you added <br>

### Exercise 4: Verifying integration between AD DS and Azure AD  

Synchronization may take up to 15 minutes until the step 2 updates with status of synchronization.  <br>

### Exercise 5: Implementing Azure AD integration features in AD DS  

## Unable to do exercise 5 due to Microsoft change to Licensing of Premium plans - Skip to Exercise 6

### If you want to see how to install the Azure AD Password Protection service on-premise do Task 5: Install and register the Azure AD Password Protection proxy service and DC agent - You can install but will be unable to register

Skip Task 6: Enable password protection in Azure <br>

## Ensure you do Exercise 6: Cleaning up

### Exercise 6: Cleaning up

Task 1: Uninstall Azure AD Connect
Step 3: Double click Microsoft Entra Connect Sync

