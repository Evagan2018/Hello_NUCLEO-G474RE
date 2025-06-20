[![License](https://img.shields.io/github/license/Arm-Examples/Hello_NUCLEO-G474RE?label)](https://github.com/Arm-Examples/Hello_NUCLEO-G474RE/blob/main/LICENSE)
[![Build and Execution Test](https://img.shields.io/github/actions/workflow/status/Arm-Examples/Hello_NUCLEO-G474RE/build.yml?logo=arm&logoColor=0091bd&label=Build%20and%20Execution%20Test)](https://github.com/Arm-Examples/Hello_NUCLEO-G474RE/tree/main/.github/workflows/build.yml)

# Hello example for NUCLEO-G474RE
[![CMSIS Compliance](https://img.shields.io/github/actions/workflow/status/Arm-Examples/Hello_NUCLEO-G474RE/verify.yml?logo=arm&logoColor=0091bd&label=CMSIS%20Compliance)](https://www.keil.arm.com/cmsis) 

Simple Hello World example for STMicroelectronics [**NUCLEO-G474RE**](https://www.st.com/en/evaluation-tools/nucleo-g474re.html) development board.
This example prints "Hello World" and a counter value via the standard output which is routed to the debug console through Virtual COM port.

[![Keil Studio Cloud - Import Project](https://img.shields.io/badge/Keil_Studio_Cloud-Import_Project-0091bd?logo=arm&logoColor=0091bd)](https://studio.keil.arm.com/?import=https://github.com/Arm-Examples/Hello_NUCLEO-G474RE.git)
[![example workflow](https://img.shields.io/github/actions/workflow/status/Arm-Examples/Hello_NUCLEO-G474RE/ci.yml?logo=arm&logoColor=0091bd&label=Example%20Publishable)](https://www.keil.arm.com/)

## Prerequisites

### Tools

- [CMSIS-Toolbox v2.9.0](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/releases) or newer
- [Microsoft Visual Studio Code](https://code.visualstudio.com/download) with Keil Studio Pack extension (optional, alternatively CLI can be used)
- [Arm Compiler 6](https://developer.arm.com/Tools%20and%20Software/Arm%20Compiler%20for%20Embedded) (automatically installed when using Visual Studio Code with vcpkg)

## Build Solution/Project

### Using Visual Studio Code with extensions

Required tools described in file 'vcpkg-configuration.json' should be automatically installed by vcpkg. You can see the status of vcpkg in the status bar.

Required CMSIS packs need to be also installed. In case a required pack is missing, a notification window will pop-up to install the missing pack.

Open the 'CMSIS' view from the side bar, select desired 'Build Type' and press the 'Build' button.

### Using Command Line Interface (CLI)

Download required packs (not required when the packs are already available) by executing the following commands:

```sh
csolution list packs -s hello.csolution.yml -m >packs.txt
cpackget update-index
cpackget add -f packs.txt
```

Build the project by executing the following command:

```sh
cbuild hello.csolution.yml
```

## Run the application

### Using Visual Studio Code with extensions

- Connect the board's ST-LINK USB to the PC (provides also power).
- Open the 'CMSIS' view from the side bar:
  - Press the 'Run' button and wait until the image is programmed and starts running.

### Using Drag-and-drop programming or external programmer and terminal

- Connect the board's ST-LINK USB to the PC (provides also power).
- Program the image (.hex) using Drag-and-drop programming or use external programmer.
- Open terminal on the PC and connect to the board's serial port with 115200 baud rate.
- Observe the terminal output.

## Debug the application

Before starting to debug the application, make sure that you have gone through the steps as described in the
[run the application](#run-the-application) section.

### Using Visual Studio Code with extensions

Open the 'CMSIS' view from the side bar and press the 'Debug' button.
