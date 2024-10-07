# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Errata All Modules

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell. <br>

## Module 01: Implementing identity services and Group Policy

### Exercise 1: Deploying a new domain controller on Server Core

Task 2: Prepare the AD DS installation and promote a remote server<br>
Step 13: Ignore the DNS delegation warning <br>
Step 17: First copy the script into the PowerShell ISE <br>
Step 20 and 21: Are the same step one with and one with out the pasted varibles <br>

### Exercise 2: Configuring Group Policy  

Task 3: Review the effects of the GPO's settings<br>  
Step 5: You may get disconnected from the VM, select Retry Connection if prompted  <br> 

Note:  You may have to do this each time you switch log in between users. <br>

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  

Ignore the note you will be able to create a tenant <br>
Step 4: Type Microsoft Entra ID and Select
Step 9: If challenged with “Help us prove you’re not a bot” enter the Captia and hit submit. <br> 

### Exercise 1:  Preparing Azure AD for AD DS integration  

Scipt lab setup as you have already completed <br>
Task 1: Create a custom domain in Azure <br>
Step 2: Use the credential provided in the lab <br>

Task 2: Create a user with the Global Administrator role <br> 
Step 2: After selecting New Users, select Creat new user <br> 
After step 4: Copy the new users User Principle Name and Password into Notepad so you can use it in later steps. 
Step 5: Click Next: Properties - Scroll sown to setting and set usage location as United States <br> 

Task 3: Change the password for the user with the Global Administrator role  <br>
Step 1: Open a New InPrivate window
Step 3 and 4: Paste the logon name and passowrd you previously copied. <br> 
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

## Unable to do remaining steps in Task 1 due to Microsoft change to Licensing of Premium plans - Skip to Task 2

Task 5: Install and register the Azure AD Password Protection proxy service and DC agent - You can install but will be unable to register <BR>
Skip Task 6: Enable password protection in Azure <br>
Ensure you do Exercise 6: Cleaning up <BR>

## Module 03:  Managing Windows Servers 

## Exercise 1: Implementing and using remote server administration
### Skip Task 1: Install Windows Admin Center

Task 4: Verify remote administration <br>
Step 1:  Stay connected to SEA-DC1 <br>

Task 5: Administer servers with Remote PowerShell <br>
Instead on PowerShell console use the PowerShell ISE <br>

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Task 1: Create an Azure resource group by using an Azure Resource Manager template <br>
Step 2.  The credentials are located on the Resources Tab at the top of the lab instructions <br>
Step 4.  Use the following steps to create the Storage > Select Mount Storage account > Select your subscription in the dropdown box > Click Apply > Select We will create storage account for you > click next <br>
Step 5.  Click Manage files to upload the files. C:\allfiles\labfiles\lab04\l04-sub_template.json<br>
Step 6:  Does not paste correctly.  Paste into notepad.  Change the first lint <Azure_Region> to EastUS. Then copy and paste from notepad into the Cloud Shellpaste the remaining lines together <br>

Task 2: Create an Azure VM by using an Azure Resource Manager template <br>
Step 1: Json files are located in C:\allfiles then the path listed <br>
Step 6: Starting address not address range  <br>

### Exercise 2: Implementing hybrid connectivity by using the Azure Network Adapter

Task 1: Register Windows Admin Center with Azure <br>
Skip steps 1 - 3 as the Windows Admin Center is already installed <br>

### Exercise 3: Deploying Windows Admin Center gateway in Azure  Does not work as written - Skip to my alternate steps 

### Alternate Steps for - Exercise 3: Deploying Windows Admin Center gateway in Azure 

### Replace Exercise 3 Task 1 steps 5 - 11 with the following

Though the script fails, I created a work-around. It does require a manual install of WAC on the az800104-vmwac, but in the real world, you would not have a script like in this lab.<br>

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

## Module 05: Implementing and configuring virtualization in Windows Server 

### Exercise 1: Creating and configuring VMs
Task 4: Manage Virtual Machines using Windows Admin Center <br>
Steps 1 - 3: The WAC is already installed on SEA-ADM1 you can skip to step 4 <br>

## Module 06 – Deploying and configuring Windows Server on Azure VMs 

### No Errata

## Module 07:  Implementing and configuring network infrastructure services in Windows Server 

### Exercise 1: Deploying and configuring DHCP 

Task 1: Install the DHCP role <br>
The WAC is already installed <br>

Task 3: Create a scope <br>
You may have to refresh the page for the DHCP tool to display <br>

Step 1:  Once you click on the DHCP tool you may be prompted to Install the PowerShell RSAT tools.  Click Install <br>

### Exercise 2: Deploying and configuring DNS 

Task 2: Create a DNS zone <br>
You may have to refresh the page for the DNS tool to display <br>

Step 1:  Once you click on the DNS tool you may be prompted to Install the PowerShell RSAT tools.  Click Install <br>

Task 5: Configure DNS policies <br>
The paste function does not paste correctly in this task.  Copy and paste them manually <br>

Task 6: Verify DNS policy functionality <br>
Step 3:  Only paste the second Cmdlet. <br>
Step 9:  Only paste the second Cmdlet. <br>

## Module 08 – Implementing hybrid networking infrastructure 

### Exercise 1: Implement virtual network routing in Azure 

Task 1: Provision lab infrastructure resources <br>
Step 6:  Copy and paste each line individually.  Replace ‘<azure_region>’ with ‘eastus’ <br>
Step 7:  Copy and paste all lines, press enter after pasting <br>
Step 8:  Copy and paste all lines, press enter after pasting <br>

Task 3: Test transitivity of virtual network peering <br>
Step 15:  Select IP Address in the Address prefix source before adding the Address Prefix <br>

### Exercise 3: Deprovisioning the Azure environment 

CloudShell commands do not paste properly, copy and paste manually <br>

## Module 09:  Implementing Storage Solutions in Windows Server

### Exercise 1: Implementing Data Deduplication 

Task 3: Test Data Deduplication <br>
Step 11, 13 sand 16:  The Cmdlet will not paste from the instructions.  Manually copy and paste. <br>

### Exercise 2: Configuring iSCSI storage 

Task 2: Connect to and configure iSCSI targets <br>
Step 6:  If the option New iSCSI Virtual Disk is greyed out close and reopen Server Manager <br>

### Exercise 3: Configuring redundant Storage Spaces 

Task 2: Create a volume based on a three-way mirrored disk <br>
Step 4:  Right click on SP1 and select New Virtual disk <br>
Step 12:  In the Virtual Disk pane <br> 

## Module 10:  Implementing Azure File Sync 

### Exercise 4: Verifying replication and enabling cloud tiering 

Task 2: Enable cloud tiering <br>
Step 5:  Paste each separately and hit enter after pasting <br>

 
