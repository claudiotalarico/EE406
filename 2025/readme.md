## References
- S. Harris and D. Harris, Digital Design and Computer Architecture, RISC-V Edition, Morgan Kaufmann, 1/e
- N. Weste and D. Harris, CMOS VLSI Design, Wiley, 4/e
- B. Murmann, [Analysis and Design of Elementary MOS Amplifier Stages](https://github.com/bmurmann/Book-on-MOS-stages)
- P. R. Gray, P. J. Hurst, S. H. Lewis, R. G. Meyer, Analysis and Design of Analog Integrated Circuits, Wiley, 6/e 
- B. Razavi, Design of Analog CMOS Integrated Circuits, McGraw Hill, 2/e
- H. Pretl, [Analog Circuit Design](https://iic-jku.github.io/analog-circuit-design/)
- R.J. Baker, CMOS Circuit Design, Layout and Simulation, Wiley 4/e - [cmos.edu](https://cmosedu.com/)

## Steps to setup the EDA Tools
### Windows OS
1. Make sure your system has the minimum requirements to support WSL2 <br><br>
   WSL 2 is only available in Windows 11 or Windows 10, Version 1903, Build 18362 or later.<br>
   For official documentation on WSL follow this [link](https://learn.microsoft.com/en-us/windows/wsl/)<br><br>
   To find the version of your Windows OS press the **`windows logo key + R`** and then type **`winver`** in the Run dialog box<br>
   or <br>
   navigate to `Start > Settings > System > About`<br><br>
   Alternatively, you can also run the following PowerShell command:
   ```
   systeminfo | findstr -r /C:"^OS Name:" /C:"^OS Version:"
   ```
   **Example**<br>
   My Surface Book 3 has:
   ```
   OS Name:                       Microsoft Windows 11 Pro
   OS Version:                    10.0.26100 N/A Build 26100
   ```
2. Install WSL2<br>
   To see the list of all avaliable Linux distribution run the following PowerShell command<br>
   ```
   wsl.exe --list --online
   ```
   To install the latest LTS Ubuntu distribution run:
   ```
   wsl.exe --install -d Ubuntu-24.04
   ```
   You will be prompted to create a UNIX username and password.<br>
   This UNIX username and password have no relationship to your Windows username and password.<br>
   To avoid any confusion use a different username<br>
   
3. Start WSL <br>
   In general, to start using WSL, open a PowerShell terminal and type:
   ```
   wsl ~
   ```
   To check which version of WSL you are running use the following PowerShell command:
   ```PowerShell
   wsl --list
   ```
   or
   ```
   wsl --list --verbose
   ```

