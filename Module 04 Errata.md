# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 4 Errata

## NOTE:  After launching lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell. <br>

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Task 1: Create an Azure resource group by using an Azure Resource Manager template <br>
Step 2.  The credentials are located on the Resources Tab at the top of the lab instructions <br>
Step 4.  Use the following steps to create the Storage > Select Mount Storage account > Select your subscription in the dropdown box > Click Apply > Select We will create storage account for you > click next <br>
Step 5.  Click Manage files to upload the files. C:\allfiles\labfiles\lab04\l04-sub_template.json<br>
Step 6:  Does not paste correctly.  Paste into notepad.  Change the first line <Azure_Region> to EastUS. Then copy and paste from notepad into the Cloud Shell<br>

Task 2: Create an Azure VM by using an Azure Resource Manager template <br>
Step 1: Json files are located in C:\allfiles then the path listed <br>
Step 6: Starting address not address range  <br>

### Exercise 2: Implementing hybrid connectivity by using the Azure Network Adapter

Task 1: Register Windows Admin Center with Azure <br>
Skip steps 1 - 3 as the Windows Admin Center is already installed <br>

### Exercise 3: Deploying Windows Admin Center gateway in Azure  Does not work as written - Skip to my alternate steps 

If the the powerShell Cmdlets do not paste correctly.  Copy and paste them into notepad first<br>

### Alternate Steps for - Exercise 3: Deploying Windows Admin Center gateway in Azure 

### Replace Exercise 3 Task 1 steps 5 - 11 with the following

Though the script fails, I created a work-around. It does require a manual install of WAC on the az800l04-vm0, but in the real world, you would not have a script like in this lab.<br>

On SEA-ADM1: <br>

In the Azure portal, search for Virtual Machines <br>
Click the link for az800l04-vm0 <br>
On the left under Settings, click Connect <br>
Click Download RDP file <br>
Click Open File <br>
Click Connect in the warning pop up window <br>
Wnen promted  <br>
Account:  Student <br>
Password: Pa55w.rd1234  <br>
click OK <br>
Click Yes <br>

Once logged in: <br>
Click NO in the Network blue pane <br>
Close any open windows <br>
Click the Start button and type Edge, click Microsoft edge <br>
Complete the Edge setup wizard <br>
In the Edge url field, type Windows Admin Center <br>
Click the first returned link <br>
Click Download Windows Admin center button <br>
Click Open file <br>
Close Edge <br>
Check the "I accept these terms" box, click Next 5 times <br>
Click Install <br>
Click Finish <br>
Right Click Start > Shut down or sign out > Disconnect <br>

Pick up on Task 2: Review results of the script provisioning <br>
Step 1: <br>
Locate the vm named az800l04-vm0 in the Azure portal <br>
Copy the public IP address on the Overview page <br>
Open a new browser tab > Right click the URL field and choose paste the public IP address, you will need to add https:// in front of the ip address<br>





