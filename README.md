# Mobiview
test
## Overview
Mobiview is a Python-based project designed to automate the retrieval and formatting of in-depth specifications from Android devices connected via ADB (Android Debug Bridge). The project leverages ADB commands and USB debugging to gather detailed device information, which is then processed and converted into an Excel workbook format for easy readability and analysis.

## Features
- Connects to Android devices using ADB and USB debugging.
- Retrieves device specifications including hardware, software, and display information.
- Converts generated JSON or .log files into a unified Excel workbook using openpyxl.
- Provides a streamlined process for accessing and visualizing device data.

## Requirements
- Python 3.x
- ADB (Android Debug Bridge)
- Cygwin (for Windows users for ADB functionality)
- PyCharm IDE (or any Python IDE)
- openpyxl library (for Excel file manipulation)

## Usage
1. **Setup Environment:**
   - Ensure Python 3.x and necessary libraries (`openpyxl`) are installed.
   - Set up ADB on your system and enable USB debugging on your Android device.

2. **Run the Program:**
   - Open PyCharm IDE and load the project.
   - Configure ADB connectivity and ensure the device is connected.
   - Run the main Python script to initiate the retrieval and conversion process.

3. **Process Overview:**
   - The program will connect to the device using ADB commands.
   - It will retrieve detailed specifications such as device information, display specs, software details, and hardware specifics.
   - The gathered data will be parsed and organized into a unified Excel sheet format.
   - The Excel workbook can then be used for further analysis or documentation purposes.

## Example
```python
# Example code snippet to demonstrate connecting to ADB and retrieving device info
import subprocess

def connect_to_adb():
    # Example ADB command
    adb_output = subprocess.check_output(["adb", "devices"])
    print(adb_output.decode('utf-8'))

def main():
    connect_to_adb()
    # Add more functionality to retrieve and process device info

if __name__ == "__main__":
    main()
