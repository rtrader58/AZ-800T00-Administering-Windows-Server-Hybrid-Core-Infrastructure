# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 4 Errata

## NOTE:  After launching lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

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

