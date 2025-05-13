# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 9 Errata 

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up because they finish starting before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>

Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PowerShell. <br>

## Module 09:  Implementing Storage Solutions in Windows Server 

### Exercise 1: Implementing Data Deduplication 

Task 3: Test Data Deduplication <br>
Step 11, 13 sand 16:  The Cmdlet will not paste from the instructions.  Manually copy and paste. <br>

### Exercise 2: Configuring iSCSI storage <br>

Task 2: Connect to and configure iSCSI targets <br>
Step 6:  If the option New iSCSI Virtual Disk is greyed out close and reopen Server Manager <br>

### Exercise 3: Configuring redundant Storage Spaces <br>

Task 2: Create a volume based on a three-way mirrored disk <br>
Step 4:  Right click on SP1 and select New Virtual disk <br>
Step 12:  In the Virtual Disk pane  <br>
 
