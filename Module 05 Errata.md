# AZ-800T00 Configuring Windows Server Hybrid Core Infrastructure - Module 5 Errata

## NOTE:  After launching each lab environment use the power commands to restart all the virtual machines with the exception of the Domain Controller.  (reason – virtual machines do not authenticate during start up because they finish starting before the DC does)  

### Known issue - Pasting from the lab instructions in PowerShell does not work in Server 2019 and 2022.<br>

Option 1:  Open PowerShell ISE and paste into the PowerShell Prompt <br>
Option 2:  Open Notepad and paste from instruction into notepad then cut and paste into PowerShell. <br>

## Module 05: Implementing and configuring virtualization in Windows Server 

### Exercise 1: Creating and configuring VMs
Task 4: Manage Virtual Machines using Windows Admin Center <br>
Steps 1 - 3: The WAC is already installed on SEA-ADM1 you can skip to step 4 <br>

When you select the Virtual Machine blade in the WAC you may see a prompt that states there is an update for that blade.  Follow the prompts to update the Virtual Machine blade <br>

### Exercise 2: Installing and configuring containers
### Make sure you are doing the steps on the correct computer

Task 1: Install Docker on Windows Server <br>
#### NOTE - Per the note at the beginning of the exercise the Windows Admin Center is to slow.  Complete the lab in the PowerShell ISE and use PowerShell PSSession to connect to SEA-SVR1
Step 2: Paste in the script block of the ISE and run <br>
Step 3: Ensure you are restarting SEA-SVR1. After restarting SEA-SVR1 switch to SEA-SVR1 to watch it start - when done, switch back to SEA-ADM1 and use the PowerShell ISE to reconnect the PowerShell PSSession to SEA-SVR1 <br>
#### Note - The script does not run when SEA-SVR1 restarts.  Paste .\install-docker-ce.ps1 in the ISE and run again
Step 5: Required to be ran on SEA-SVR1 add the following steps <br>
Step 5a: Switch to SEA-SVR1 > Logon and Type 15 to close the MSCONFIG windos <br>
Step 5b: Type notepad to open notepad <br>
Step 5c: Paste the command into notepad then copy and paste into the PowerShell prompt <br>
Steps 9 - 13:Paste the command into notepad then copy and paste into the PowerShell prompt <br>
Step 9: Paste into notepad then replace <containerID> with the actual containerID listed in the previous step <br>
Skip Step 13: <br>

Task 3: Use Windows Admin Center to manage containers <br>
Step 2: Install the Container update, by seclecting Containers and then Install if available <br>
