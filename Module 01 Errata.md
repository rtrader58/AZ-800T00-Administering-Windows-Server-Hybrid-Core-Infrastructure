# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 1 Errata

## NOTE:  After launching lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start because they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PowerShell. <br>

## Module 01: Implementing identity services and Group Policy

### Exercise 1: Deploying a new domain controller on Server Core

Task 2: Prepare the AD DS installation and promote a remote server<br>
Step 13: Ignore the DNS delegation warning <br>
Step 17: First copy the script into the PowerShell ISE <br>
Step 20 and 21: Are the same step one with and one with out the pasted varibles <br>

### Exercise 2: Configuring Group Policy  

Task 3: Review the effects of the GPO's settings<br>  
Step 5: You may get disconnected from the VM, select Retry Connection if prompted <br> 

Note:  You may have to do this each time you switch log in between users. <br>


