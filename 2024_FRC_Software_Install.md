# 2024 FRC Software Install

Setting up all of the components for WPILib development is fully documented in [FRC Game Manual - Step 2: Installing Software](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/index.html). The steps are summarized here, but always refer to the WPILib documentation if there is any question about what to do.

## 1. Install the NI FRC Game Tools
*This is only needed on computers that will be used as a driver station. They aren't necessary for simply programming the robot.*

1. Download **FRC Game Tools 2024** from the link to NI provided in the Requirements section of [Installing the FRC Game Tools](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/frc-game-tools.html).
2. Follow the [Installation](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/frc-game-tools.html#installation) instructions.
3. Reboot the computer

---
## 2. Install WPILib

To program the robot, you will need to install WPILib. This installs a customized VSCode development environment and all of the libraries necessary to program the RoboRio. The installation is done in it's own sandbox and will not overwrite prior year's WPILib installs or your own version of VSCode if you use it. 

1. Follow the instructions in the [WPILib Installation Guide](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html) to download and install WPILib.
2. 

### WPILib VSCode Configuration Changes
*These are some options that should be changed from the defaults*

Press *Ctrl + ,* to open the setting dialog, then search for these settings:
- Turn on Autosave: `files.autosave: afterDelay`

---
## 3. Install Vendor Deps

Vendordeps contain specific code extensions necessary to interface with hardware other than the RoboRio. You may have trouble installing some of these over the school WiFi. Instead, do this step at home or on a personal hotspot, or request help with the offline install process.

Most vendordeps are listed on the [3rd Party Libraries](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html#rd-party-libraries) page. When you need a library, you should follow the [Installing Libraries](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html#installing-libraries) instructions for that particular library. You only need to install libraries for components that you are actually using on the robot. Once you've installed the library in a repo, it will automatically be downloaded to other computers that clone that repo as long as they are connected to the internet when they run the build process.

Here are some that we commonly use:
* **REV Robotics REVLib** - for SparkMax motor controller, and PDH Power Delivery Hub
* **Kauai Labs** - for NavX2 gyro
* **CTRE Phoenix Framework** - Install v6 (and v5 for Talon motor controller support)
* **PhotonVision** - computer vision software that runs on a coprocessor
* [Full List of Vendor Libraries](https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html#vendor-libraries) - in case you are looking for others

---
## 4. Addtional Software Tools

### [Git for Windows](https://gitforwindows.org/) *Recommended*
Powerful command line tool to have for managing git repos and synchronizing with GitHub. You can accept all the defaults when it installs.

### [GitHub Desktop](https://desktop.github.com/) *Recommended*
Graphical user interface for managing repos synced with GitHub.

### [Balena Etcher](https://www.balena.io/etcher/) 
Used for flashing the µSD for the RoboRio2 and Raspberry Pi.

### [REV Hardware Client](https://docs.revrobotics.com/rev-hardware-client/) 
Used for managing firmware on the Rev components (SparkMax). 

### [FRC Radio Configuration Utility](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/radio-programming.html) 
This is a special utility for configuring the radio. It is awkward to use and only needs to be installed on one or two computers. 