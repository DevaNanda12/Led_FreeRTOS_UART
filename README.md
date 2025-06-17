# STM32 FreeRTOS UART and LED Toggle Example

## Overview
This project demonstrates a basic FreeRTOS application running on an STM32 microcontroller (e.g., STM32F4 series). It includes:

- Initialization of the system clock, GPIO, and USART2 peripheral.
- Creation of three FreeRTOS tasks:
  - **Default Task:** An idle task that runs continuously with minimal activity.
  - **LED Task:** Toggles an LED connected to GPIO pin PA5 every 500 ms.
  - **UART Task:** Transmits the string `"Hello\r\n"` over USART2 every 1 second.

The project uses the STM32 HAL (Hardware Abstraction Layer) library and CMSIS-OS (FreeRTOS) for task scheduling.

---

## Features
- System clock configured to use HSI oscillator.
- GPIO initialization for LED output on pin PA5.
- UART2 initialized at 115200 baud for serial communication.
- Three concurrent FreeRTOS tasks demonstrating multitasking:
  - LED blinking task.
  - UART transmission task.
  - Default idle task.
- Basic error handling with infinite loop on HAL errors.

---

## File Structure
- **main.c**: Main application code, including peripheral initialization and FreeRTOS task definitions.
- **main.h**: Header file with function prototypes and peripheral handles.
- HAL and CMSIS-OS libraries are required for compilation.

---

## Usage
1. Build and flash the firmware to your STM32 development board.
2. Connect the UART2 pins to a serial terminal configured at 115200 baud.
3. Observe the onboard LED toggling every 500 ms.
4. Monitor the serial terminal for the "Hello" message transmitted every second.

---

## Notes
- This example uses the internal HSI oscillator without PLL for simplicity.
- Modify GPIO pin definitions and UART settings as per your hardware.
- Ensure FreeRTOS and STM32 HAL libraries are correctly integrated into your project.

---

## License
This software is provided **AS-IS** under the terms specified in the LICENSE file (if available).

---
## Author

- Deva Nanda S
