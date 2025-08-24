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
1. Make sure your system have the minimum requirements to support WSL2
documentation[https://learn.microsoft.com/en-us/windows/wsl/]

  To find the version of your Windows OS press `windows key + R` and then type `winver` in the Run dialog   box or navigate to `Start > Settings > System > About` <br>
  Alternatively, you can also run the following PowerShell command:
  ```
  systeminfo | findstr -r /C:"^OS Name:" /C:"^OS Version:"
  ```

  **Example**<br>
  The PC I am using has:
  ```
  OS Name:                       Microsoft Windows 11 Pro
  OS Version:                    10.0.26100 N/A Build 26100
  ```
2. Install WSL2
To see the list of all avaliable Linux distribution run the following PowerShell command<br>
```
wsl.exe --list --online
```
To install the latest LTS Ubuntu distribution run:
```
wsl.exe --install -d Ubuntu-24.04
```

