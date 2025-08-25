## References
- S. Harris and D. Harris, Digital Design and Computer Architecture, RISC-V Edition, Morgan Kaufmann, 1/e
- N. Weste and D. Harris, CMOS VLSI Design, Wiley, 4/e
- B. Murmann, [Analysis and Design of Elementary MOS Amplifier Stages](https://github.com/bmurmann/Book-on-MOS-stages)
- P. R. Gray, P. J. Hurst, S. H. Lewis, R. G. Meyer, Analysis and Design of Analog Integrated Circuits, Wiley, 6/e 
- B. Razavi, Design of Analog CMOS Integrated Circuits, McGraw Hill, 2/e
- H. Pretl, [Analog Circuit Design](https://iic-jku.github.io/analog-circuit-design/)
- R.J. Baker, CMOS Circuit Design, Layout and Simulation, Wiley 4/e - [cmos.edu](https://cmosedu.com/)

## Steps to setup the EDA Tools on Windows OS

1. **Make sure your system has the minimum requirements to support WSL 2** <br><br>
   WSL 2 is only available in Windows 11 or Windows 10, Version 1903, Build 18362 or later.<br>
   For the official documentation on WSL follow this [link](https://learn.microsoft.com/en-us/windows/wsl/)<br><br>
   To find the version of your Windows OS press the **`windows logo key + R`** and then type **`winver`** in the Run dialog box<br>
   or <br>
   navigate to `Start > Settings > System > About`<br><br>
   Alternatively, you can also run the following PowerShell command:
   ```
   systeminfo | findstr -r /C:"^OS Name:" /C:"^OS Version:"
   ```
   **Example**<br>
   I am using a Surface Book 3 with:
   ```
   OS Name:                       Microsoft Windows 11 Pro
   OS Version:                    10.0.26100 N/A Build 26100
   ```
2. **Install WSL 2**<br>
   To see the list of all avaliable Linux distribution use the following PowerShell command:<br>
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
 
3. **Start WSL**<br>
   In general, to start using WSL, either open a PowerShell terminal and type:
   ```
   wsl ~
   ```
   or select the Ubuntu app in the Window's Start Menu.<br>
   The Linux user's home directory is:<br>
   `/home/<linux username>`<br>
   The Windows user's home directory is:<br>
   `/mnt/c/Users/<windows username>`<br><br>
   **Example**<br>
   >`talarico@TALARICO-SRFCBK:~$ pwd`<br>
   >`/home/talarico`
   
   >`talarico@TALARICO-SRFCBK:~$ cd /mnt/c/Users/claudio/`<br>
   >`talarico@TALARICO-SRFCBK:/mnt/c/Users/claudio$`
   
   To check which version of WSL you are running use the following PowerShell command:
   ```
   wsl --list
   ```
   or
   ```
   wsl --list --verbose
   ```
   It is recommended that you regularly update and upgrade your packages:
   ```
   sudo apt update -y && sudo apt upgrade -y
   ```
3. **WSL and GUI apps**<br><br>
   Since 2025-08-06 WSL supports running Linux GUI applications (X11 and Wayland) on Windows.<br><br>
   X11 has been the dominant display server protocol for Unix-like windowing systems.<br>
   Wayland was introduced in 2008 as a new protocol and a modern replacement for X11.<br>
   To install the apps and tools that ship with X11 run:<br> 
   ```
   sudo apt install x11-apps -y
   ```
   ```
   sudo apt install xterm -y
   ```
   and add the following line:
   ```
   export LC_ALL=C
   ```
   to the `~/.bashrc` file.<br>

   WSL 2 enables Linux GUI applications to be used on Windows and allows to:
   - Launch Linux apps from the Windows Start menu
   - Pin Linux apps to the Windows task bar
   - Use alt-tab to switch between Linux and Windows apps
   - Cut + Paste across Windows and Linux apps

4. **Accessing the WSL file system from Windows**<br>
   From the Power Shell terminal run the following command:<br>
   `explorer \\wsl$\Ubuntu-24.04\home\<linux username>`

5. **Accessing the Windows file system from WSL**<br>
   To make it easier to navigate the windows file system, cosider adding symbolic links.<br><br>
   **Example**<br>
      ```
      ln -s /mnt/c/Users/claudio ~/whome
      ```
      ```
      ln -s /mnt/c/Users/claudio/icloudDrv/iCloudDrive ~/ihome
      ```
6. **[Install Docker Desktop on Windows](https://docs.docker.com/desktop/setup/install/windows-install/)**
7. **Start Docker Desktop**<br>
   Start Docker and open Settings at the top menu bar. Go to Resources → WSL Integration and enable Ubuntu-24.04. This will allow us to run Docker in Ubuntu WSL terminal.
8. **Clone the [iic-osic-tools](https://github.com/iic-jku/IIC-OSIC-TOOLS) container onto your WSL user's home folder**
   ```
   cd ~
   git clone --depth=1 https://github.com/iic-jku/iic-osic-tools.git
   ```
9. **Browse to the iic-osic-tools directory**<br>
   ```
   cd ~/iic-osic-tools
   ```

10. **Start the container using the script `./start_x.sh`**<br>
    But ..., before we can successfully run the script `./start_x.sh` there are a few more steps that needs to be to completed:
    1. Install and run an Xserver for Windows (MobaXterm)
    2. Set the DESIGNS variable inside `./start_x.sh`
    3. Install Linux packages
   
11. **Install and start [MobaXterm Home Edition](https://mobaxterm.mobatek.net/download.html)** <br>
    Among its many features MobaXterm provides a fully configured Xserver with built-in X11 forwarding to display graphical applications



