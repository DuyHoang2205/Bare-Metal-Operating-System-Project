# Bare Metal Operating System Project 

## Overview

This project involves the development of a **Bare Metal Operating System** (OS) for the **Raspberry Pi 4**. The goal of the project was to implement basic OS features such as a **Command Line Interpreter (CLI)**, **image/video/text display**, and a **game application** running on a Bare Metal OS.

The project is divided into three major tasks:

1. **Welcome Message & Command Line Interpreter (CLI)**
2. **Image, Video, and Text Display**
3. **Game Development for Bare Metal OS**

This README provides an overview of the tasks and installation instructions.

---

## Table of Contents
- [System Overview](#system-overview)
- [Task 1: Command Line Interpreter (CLI)](#task-1-command-line-interpreter-cli)
- [Task 2: Image, Video, and Text Display](#task-2-image-video-and-text-display)
- [Task 3: Game Development for Bare Metal OS](#task-3-game-development-for-bare-metal-os)
- [Installation & Setup](#installation-setup)
- [Usage](#usage)
- [License](#license)

---

## System Overview

This project demonstrates the use of a **Bare Metal OS** on a **Raspberry Pi 4**. The OS includes basic functionalities such as **CLI commands**, **image and video display**, and **game interaction**. Each task focuses on specific features of OS and peripheral driver development.

---

## Task 1: Command Line Interpreter (CLI)

The **CLI** allows users to interact with the OS through text commands, similar to terminal environments like **Linux Shell** or **Windows PowerShell**. Key features of the CLI include:

- **OS Name Display**: Displays the OS name in the console while waiting for user input.
- **Command History**: Users can browse command history using the **UP** and **DOWN** keys (re-mapped to `_` and `+`).
- **Auto-Completion**: TAB key auto-completes commands.
- **Commands**:
  - **help**: Shows information about commands.
  - **clear**: Clears the terminal screen.
  - **showinfo**: Displays board revision and MAC address.
  - **baudrate**: Changes the UART baud rate.
  - **stopbit**: Changes the stop bit configuration of the UART.

---

## Task 2: Image, Video, and Text Display

This task involved displaying **images** and **videos** on the screen along with **text**. The key requirements were:

1. **Image Display**:
   - Displaying background images with the team members’ names.
   - Converted image data into **ARGB32 format** using tools like **image2cpp**.
   
2. **Text Display**:
   - Custom fonts were created to display team information and other text elements on the screen.

3. **Video Display**:
   - Displaying short **video clips** by converting frames into **ARGB32 format** and displaying them in sequence.

---

## Task 3: Game Development for Bare Metal OS

For the final task, we developed a basic game, **Sokoban**, on the Bare Metal OS. The game mechanics and user interactions were implemented using the following features:

- **Game Description**:
  - Sokoban is a puzzle game where the player moves boxes to designated storage locations in a warehouse.
  - The player uses arrow keys (mapped to UART commands) to move the character and push boxes.

- **Game Development**:
  - The game features multiple levels with a fixed start state.
  - **Game Input**: Movement commands are sent from the terminal using `W`, `A`, `S`, `D` keys.
  - **Game Output**: The game state is displayed on the screen, with real-time updates for the player's progress.
  
- **Communication**: The game communicates with the CLI through UART, sending character inputs and receiving acknowledgments.

---

## Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/DuyHoang2205/Bare-Metal-Operating-System-Project.git
   cd Bare-Metal-Operating-System-Project
   ```
2. **Build the project:**
The project uses Make as the build system. Run the following command to compile the source code:
    ```bash
    make
    ```
This will create the kernel8.img file, which is the Bare Metal OS image that will run on the Raspberry Pi 4.
3. **Set up UART communication:**
If you need to use a UART-to-USB adapter to communicate with the Raspberry Pi 4, connect the UART adapter and configure the terminal software (e.g., Tera Term or PuTTY) to match the baud rate and settings in your project
