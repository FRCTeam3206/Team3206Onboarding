# 2023 FRC Software Offline Install

## 1. Install the NI FRC Game Tools
*This is only needed on computers that will be used as a driver station. They aren't necessary for simply programming the robot.*

1. Mount the ISO: `ni-frc-2023-game-tools_23.0.0_offline.iso`
2. Run the installer and follow the [instructions for installing the FRC Game Tools](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/frc-game-tools.html)
3. Enter the serial number when requested:
    > Serial Number:  **B05P17699**
4. Reboot the computer

---
## 2. Install WPILib

1. Mount the ISO `WPILib_Windows-2023.1.1.iso` and run the installer
2. On the first screen, select "Install for this User" option
3. On the second screen, select "Select existing VS Code zip for offline install on this computer" and select `WPILib-VSCode-1.74.2.zip` from the USB stick with the offline files
4. Unmount the ISO (or reboot)

### VSCode Configuration Changes
*These are some options that should be changed from the defaults*

Press *Ctrl + ,* to open the setting dialog, then search for these settings:
- Turn on Autosave: `files.autosave: afterDelay`
- Turn off inlay hints: `editor.inlayhints.enabled: off (or offUnlessPressed)`

---
## 3. Install Vendor Deps
*Offline Installers are in the `Vendordeps` folder*

* [CTRE (for Talon, PDP, and PCM)](https://store.ctr-electronics.com/software/) - Installs the Phoenix Framework and Phoenix Tuner v1. 
    * Offline Installer: `CTRE_Phoenix_Framework_v5.30.2.1.exe`
    * The newer [Phoenix TunerX](https://pro.docs.ctr-electronics.com/en/stable/docs/tuner/index.html) is only available through the [Microsoft Store (link)](https://www.microsoft.com/store/productId/9NVV4PWDW27Z).
* [Kauai Labs (NavX)](https://pdocs.kauailabs.com/navx-mxp/software/roborio-libraries/)
    * Offline Installer: *Not released yet*
* [REVLib (for Spark Max)](https://docs.revrobotics.com/sparkmax/software-resources/spark-max-api-information#c++-and-java)
    * Offline Install: Expand `REVLib-offline-v2023.1.1.zip` into `C:\Users\Public\wpilib\2023`
* [Full List of Vendor Libraries](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html#libraries) - in case you are looking for others

---
## 4. Addtional Software Tools
*These files are in the `Additional Tools` folder*

### [Git for Windows](https://gitforwindows.org/) *Recommended*
Powerful command line tool to have for managing git repos and synchronizing with GitHub. You can accept all the defaults when it installs.

- Installer: `Git-2.39.0.2-64-bit.exe`

### [GitHub Desktop](https://desktop.github.com/) *Recommended*
Graphical user interface for managing repos synced with GitHub.

- Installer: `GitHubDesktopSetup-x64.exe`

*add instructions for connecting to the FRC github account*

### [Balena Etcher](https://www.balena.io/etcher/) 
Used for flashing the µSD for the RoboRio2 and Raspberry Pi.

- Installer: `balenaEtcher-Setup-1.13.1.exe`

### [REV Hardware Client](https://docs.revrobotics.com/rev-hardware-client/) 
Used for managing firmware on the Rev components (SparkMax). 

- Installer: `REV-Hardware-Client-Setup-1.5.0.exe`

To install the hardware profiles offline, copy the files from the `REV Firmware` directory to:

`%userprofile%\AppData\Roaming\REV Hardware Client\downloads`

*NOTE: The school WiFi network blocks access to the REV update server, so you must connect to the Ethernet or other network to update this program or the firmware.*

### [FRC Radio Configuration Utility](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/radio-programming.html#programming-your-radio) 
This is a special utility for configuring the radio. It is awkward to use and only needs to be installed on one or two computers. 

- Installer: `FRC_Radio_Configuration_23_0_2.exe`
- Installation and useage instructions: [Programming Your Radio](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/radio-programming.html#install-the-software)