# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Errata All Modules

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell. <br>

## Module 01: Implementing identity services and Group Policy  

### Exercise 1: Deploying a new domain controller on Server Core

Task 2: Prepare the AD DS installation and promote a remote server<br>
After step 25, type A then hit enter <br>

### Exercise 2: Configuring Group Policy  

Task 3: Review the effects of the GPO's settings<br>
Step 5: You may get disconnected from the VM, select Retry Connection if prompted  <br> 

Note:  You may have to do this each time you switch log in between users. <br>

## Module 02:  Implementing integration between AD DS and Azure AD  

## Lab Setup:  

Step 9: If challenged with “Help us prove you’re not a bot” enter the Captia and hit submit. <br> 

### Exercise 1:  Preparing Azure AD for AD DS integration  

Task 1: Create a custom domain in Azure <br>
Step 2: Use the credential used to redeem the Azure Pass  <br>

Task 2: Create a user with the Global Administrator role <br> 

Step 2: After selecting New Users, select Creat new user <br> 
Step 4: Show password has been removed, remove check to Auto-generate password. Create a password you will remember (recommend Pa55w.rd1234) <br> 
Step 5: Click Next: Properties - Scroll sown to setting and set usage location as United States <br> 
Step 6: click Next: Assignments - click Add Role - select Global Administrator - click select <br> 
Skip step 7:  <br> 
Step 8: Click Review and Create - click create <br> 

After step 8, click on the new user you created and copy the new users User Principle Name.  I recommend you open Notepad on your computer connecting to the lab environment and paste the account so you can use it in future labs. <br> 

Task 3: Change the password for the user with the Global Administrator role  <br><br>
Step 3:  Paste the logon name you previously copied. <br> 

### Exercise 4: Verifying integration between AD DS and Azure AD  

Synchronization may take up to 15 minutes until the step 2 updates with status of synchronization.  <br>

### Exercise 5: Implementing Azure AD integration features in AD DS  

## Unable to do remaining steps in the lab due to Microsoft change to Licensing of Premium plans

Task 1: Enable self-service password reset in Azure<br> 
Step 12:  It may take up to 15 minutes before Password Reset is available after activating the P2 subscription.  Try refreshing the screen <br>

Task 5: Install and register the Azure AD Password Protection proxy service and DC agent <br> 
Steps 7, 8 and 9 the CMDlets need to be copied and pasted as individual commands.  If needed, when pasting the commands remove the >> at the end<br>
Step 7:  When pasting the 2nd and 3rd  line change the .msi to .exe <br>
Step 8: Wait approximately 5 minutes before running the restart command to allow the Agent to install <br>

## Module 03:  Managing Windows Servers 

### No Errata 

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Step 6:  Does not paste correctly.  Paste the top 2 lines individually.  Then paste the remaining lines together <br>

### Exercise 3: Deploying Windows Admin Center gateway in Azure 

If the the powerShell Cmdlets do not paste correctly.  Copy and paste them <br>

Step 6: replace the script parametes with the following <br>

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

 
