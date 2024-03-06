# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 4 Errata

## NOTE:  After launching lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022<br>
Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell. <br>

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Step 6:  Does not paste correctly.  Paste the top 2 lines individually.  Then paste the remaining lines together <br>
<br>

### Exercise 3: Deploying Windows Admin Center gateway in Azure  Does not work as written - Skip to my alternate steps 

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

### Alternate Steps for - Exercise 3: Deploying Windows Admin Center gateway in Azure 

### Replace Exercise 3 Task 1 with the following

Though the script fails, I created a work-around. It does require a manual install of WAC on the az800;04-vmwac, but in the real world, you would not have a script like in this lab.<br>

On SEA-ADM1: <br>

In the Azure portal, search for Virtual Machines <br>
Click the link for az800l04-vmwac <br>
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
Locate the vm named az800l04-vmwac in the Azure portal <br>
Copy the DNS name on the Overview page <br>
Open a new browser tab <br>
Right click the URL field and choose paste <br>
Put https:// in the front of the url and then press Enter <br>

Continue with Ex 4, Task 1 step 2 in the lab steps <br>

