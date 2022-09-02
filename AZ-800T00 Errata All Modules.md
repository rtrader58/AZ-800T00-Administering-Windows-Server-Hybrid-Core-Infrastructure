# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Errata All Modules

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

## Module 01: Implementing identity services and Group Policy  

### Exercise 2: Configuring Group Policy  

Task 3: Review the effects of the GPO's settings  
Step 5:  You may get disconnected from the VM, select Retry Connection if prompted  

Note:  You may have to do this each time you switch log in between users.   

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  

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

## Module 03:  Managing Windows Servers 

### No Errata 

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Step 6:  Does not paste correctly.  Paste the top 2 lines individually.  Then paste the remaining lines together 

### Exercise 3: Deploying Windows Admin Center gateway in Azure 

Task 1: Install Windows Admin Center gateway in Azure 
You can temporarily downgrade the Az.Compute module version in Cloud Shell. The change is not persistent, so when you spin up a new instance of cloud shell the latest version of Az.Compute module will be used again. The process is extremely simple: 

### install the required version by typing the following commands in the cloud shell
 
Install-Module -Name Az.Compute -Force -RequiredVersion 4.23.0 

### To reload the session so the new module is used type the following

pwsh 

### To verify the version is correct type the following

Get-Module -Name Az.Compute 

Note:  Unless you click the X button to close the cloud shell, the 4.23.0 version will be used. 

Remaining steps:  If the the powerShell Cmdlets does not paste correctly.  Copy and paste them 

Step 6: replace the script parametes with the following 

$scriptParams = @{ <br>
ResourceGroupName = $rgName <br>
Name = 'az800l04-vmwac' <br>
VirtualNetworkName = $vnetName <br>
SubnetName = $subnetName <br>
PublicIPAddressName = $pipname<br> 
SecurityGroupName = $nsgname <br>
GenerateSslCert = $true <br>
size = $size <br>
} <br>

## Module 05: Implementing and configuring virtualization in Windows Server 

### No Errata 

## Module 06 – Deploying and configuring Windows Server on Azure VMs 

### No Errata 

## Module 07:  Implementing and configuring network infrastructure services in Windows Server 

### Exercise 1: Deploying and configuring DHCP 

Task 1: Install the DHCP role 
The WAC is already installed 

Task 3: Create a scope 
You may have to refresh the page for the DHCP tool to display 

Step 1:  Once you click on the DHCP tool you may be prompted to Install the PowerShell RSAT tools.  Click Install 

### Exercise 2: Deploying and configuring DNS 

Task 2: Create a DNS zone 
You may have to refresh the page for the DNS tool to display 

Step 1:  Once you click on the DNS tool you may be prompted to Install the PowerShell RSAT tools.  Click Install 

Task 5: Configure DNS policies 
The paste function does not paste correctly in this task.  Copy and paste them manually 

Task 6: Verify DNS policy functionality 
Step 3:  Only paste the second Cmdlet. 
Step 9:  Only paste the second Cmdlet. 

## Module 08 – Implementing hybrid networking infrastructure 

### Exercise 1: Implement virtual network routing in Azure 

Task 1: Provision lab infrastructure resources 
Step 6:  Copy and paste each line individually.  Replace ‘<azure_region>’ with ‘eastus’ 
Step 7:  Copy and paste all lines, press enter after pasting 
Step 8:  Copy and paste all lines, press enter after pasting 

Task 3: Test transitivity of virtual network peering 
Step 15:  Select IP Address in the Address prefix source before adding the Address Prefix 

### Exercise 3: Deprovisioning the Azure environment 

CloudShell commands do not paste properly, copy and paste manually 

## Module 09:  Implementing Storage Solutions in Windows Server 

### Exercise 1: Implementing Data Deduplication 

Task 3: Test Data Deduplication 
Step 11, 13 sand 16:  The Cmdlet will not paste from the instructions.  Manually copy and paste. 

### Exercise 2: Configuring iSCSI storage 

Task 2: Connect to and configure iSCSI targets 
Step 6:  If the option New iSCSI Virtual Disk is greyed out close and reopen Server Manager 

### Exercise 3: Configuring redundant Storage Spaces 

Task 2: Create a volume based on a three-way mirrored disk 
Step 4:  Right click on SP1 and select New Virtual disk 
Step 12:  In the Virtual Disk pane  

## Module 10:  Implementing Azure File Sync 

### Exercise 4: Verifying replication and enabling cloud tiering 

Task 2: Enable cloud tiering 
Step 5:  Paste each separately and hit enter after pasting 

 