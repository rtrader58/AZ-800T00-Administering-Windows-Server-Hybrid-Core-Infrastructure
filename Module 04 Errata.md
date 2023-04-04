# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 4 Errata

## NOTE:  After launching lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up do to they start before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.  Open Notepad and paste from instruction into notepad then cut and paste into PoserShell.

## Module 04:  Using Windows Admin Center in hybrid scenarios 

### Exercise 1: Provisioning Azure VMs running Windows Server 

Step 6:  Does not paste correctly.  Paste the top 2 lines individually.  Then paste the remaining lines together <br>
<br>

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

