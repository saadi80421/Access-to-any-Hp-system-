Access to Any laptop or computer
Using this method allow any individual to access any Laptop or Computer that hace HP BIOS installed on it 

Background story:

One time while I was using my laptop and playing a game, it suddenly shut down. When I tried to power it on again, it would automatically shut down repeatedly. After 3–4 attempts, the laptop finally powered on and took me to the Automatic Repair screen. In the Advanced Options, I explored every option one by one. Everything seemed fine—except for the "System Image Recovery" option.

In this option, the system allows users to access the owner's files without authentication. After repairing my Windows installation, I researched this option online. On GitHub and Reddit, I found some concerning information: by using this recovery feature, someone can open the system, browse and copy files, and even access the internet. This appears to be a serious vulnerability, either in the BIOS system or possibly within Windows recovery features.

Detailed Exploitation Steps:

v  Power on the laptop and enter the BIOS menu by pressing the appropriate key.

v  Press F11 to access System Recovery.

v  Navigate to Advanced Recovery Options and select System Image Recovery.

v  Proceed through the steps until you can access the Install Local Drive option.

v  Open Local Drive C, navigate to the System32 folder.

v  Rename Utilman.exe to something else and rename cmd.exe to Utilman.exe.

v  Restart the laptop.

v  On the login screen, click the Utility Manager icon — this opens a command prompt.

v  Run the following commands:

control userpasswords2

v  In the user management window, navigate to advanced settings and reset or set a password for the Administrator account.

v  Run this command in the command prompt:

  net user administrator /active:yes

 

v  Restart the laptop. You will now see an Administrator account on the login screen. Log in using the password you just set, and full access is granted — no prior credentials required
