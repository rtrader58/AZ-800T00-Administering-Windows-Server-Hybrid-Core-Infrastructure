# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 4 Errata

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up because they finish starting before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>

Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PowerShell. <br>

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Task 1: Create an Azure resource group by using an Azure Resource Manager template <br>
Step 2.  The credentials are located on the Resources Tab at the top of the lab instructions <br>
Step 4.  Use the following steps to create the Storage > Select Mount Storage account > Select your subscription in the dropdown box > Click Apply > Select We will create storage account for you > click next <br>
Step 5.  Click Manage files to upload the files. C:\allfiles\labfiles\lab04\l04-sub_template.json<br>
Step 6:  Does not paste correctly.  Paste into notepad.  Change the first line <Azure_Region> to EastUS. Then copy and paste from notepad into the Cloud Shell<br>

Task 2: Create an Azure VM by using an Azure Resource Manager template <br>
Step 1: Json files are located in C:\allfiles then the path listed <br>
Step 3: adminusername Student, Use the Password from the resources tab (Note passwword must be 12 characters - add 1234)
Step 6: Starting address not address range  <br>

### Exercise 2: Implementing hybrid connectivity by using the Azure Network Adapter

Task 1: Register Windows Admin Center with Azure <br>
Skip steps 1 - 10 as the Windows Admin Center is already installed <br>
Step 12: Create an Azure resource group by using an Azure Resource Manager template <br>

### Exercise 3: Deploying Windows Admin Center gateway in Azure  Does not work as written - Skip to my alternate steps 

If the the powerShell Cmdlets do not paste correctly.  Copy and paste them into PowerShell ISE first<br>

Step 9:  User is Student, Password it the password you created when you created the VM <br>

### Exercise 4: Verifying functionality of the Windows Admin Center gateway in Azure

Task 1: Connect to the Windows Admin Center gateway running in Azure VM
Step 4: User is Student, Password it the password you created when you created the VM <br>






