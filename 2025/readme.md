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
Check your Windows OS support WSL2.

Alternatively, run the following PowerShell command:
```
systeminfo | findstr -r /C:"^OS Name:" /C:"^OS Version:"
```
**Example**<br>
The PC I am using has:
```
OS Name:                       Microsoft Windows 11 Pro
OS Version:                    10.0.26100 N/A Build 26100
```
To see a list of all avaliable Linux distribution available<br>
```
wsl.exe --list --online
```
Install the latest LTS Ubuntu distribution:
```
wsl.exe --install Ubuntu-24.04
```
