[العربي](./15-os-and-embedded-systems_ar.md)

# <a name="-15-os--embedded-systems"></a>💻 Chapter 15: OS & Embedded Systems

## 1. What is it?

This chapter covers two interconnected fields:

* Operating Systems (OS): The core software that acts as an intermediary between computer hardware and the user/applications. It manages all the device's resources (processor, memory, storage) and provides a stable platform for all other programs to run on.
  * Best Analogy: The OS is the "government" and "civil infrastructure" of the country (the computer), managing resources and providing essential services.
* Embedded Systems: Specialized computer systems—a combination of hardware and software—designed to perform a single, specific function within a larger mechanical or electrical system.
  * Best Analogy: It's the small, dedicated computer inside your microwave, or the engine control unit in your car.

## 2. What does the specialist do?

* OS Engineer / Kernel Developer: A highly specialized software engineer who designs, builds, and maintains the "Kernel" of the operating system. They work with low-level programming languages (C, Assembly), manage hardware interactions, and focus on performance, stability, and security at the deepest level.
* Embedded Systems Engineer: A hybrid engineer who works at the intersection of hardware and software. They write software for microcontrollers and resource-constrained devices, may design electronic circuits, and integrate software with physical components.

## 3. Sub-domains

* Operating Systems: Kernel development, Driver development, Filesystem development, OS security.
* Embedded Systems: Firmware development, Real-Time Operating Systems (RTOS), Internet of Things (IoT) devices, automotive software, robotics.

## 4. Expanded Key Concepts

* OS Concepts:
  * `Kernel`: The heart of the OS. `Monolithic Kernel` (like Linux, all services in kernel space) vs. `Microkernel` (very small kernel, services in user space).
  * `Process & Thread`: A "process" is a program in execution. A "thread" is a lightweight path of execution within a process.
  * `Concurrency & Parallelism`: "Concurrency" is dealing with multiple tasks at the same time (can be on a single processor core). "Parallelism" is running multiple tasks at the same instant (requires multiple processor cores).
  * `Scheduling`: The algorithm the kernel uses to decide which process or thread gets to use the CPU at any given time.
  * `Memory Management`: How the OS allocates RAM to different processes. Includes concepts like Virtual Memory and Paging.
  * `System Calls`: The interface through which user-space programs request services from the kernel (like opening a file).
* Embedded Systems Concepts:
  * `Microcontroller (MCU)` vs. `Microprocessor (MPU)`: An MCU is a small computer on a single chip with its own memory and storage (like Arduino). An MPU is just the processor and needs external components (like Raspberry Pi).
  * `Real-Time Operating System (RTOS)`: An OS designed for systems that require timely and deterministic responses (like car brakes).
  * `Firmware`: Software that is permanently programmed onto a hardware device.
  * `Interrupts`: A signal from a hardware device to the processor, forcing it to stop its current task and handle the event (like a button press).

## 5. Expanded Tools & Technologies

* OS Development: C, Assembly, Debuggers like GDB, Compilers like GCC.
* Embedded Systems Development:
  * Languages: C, C++, MicroPython.
  * Hardware: Arduino, Raspberry Pi, ESP32.
  * Communication Protocols: I2C, SPI, UART.
  * Tools: PlatformIO (IDE), Oscilloscope, Logic Analyzer.

## 6. In-Depth Workflow

Project: Build a simple embedded system for a Smart Thermostat.
Hardware: ESP32 microcontroller, DHT11 temperature sensor, and a Relay module to control an air conditioner.

 1. Circuit Design: The engineer connects the temperature sensor and the Relay to the correct GPIO pins on the ESP32 board.
 2. Setup Development Environment: They use PlatformIO within VS Code to write, compile, and upload the code to the ESP32.
 3. Write the Firmware in C++:
     * `setup()` function: Initializes serial communication for debugging, sets the sensor pin as an input, and the relay pin as an output.
     * `loop()` main loop:
         * Read the temperature from the DHT11 sensor.
         * Compare the current temperature to the target temperature (e.g., 24°C).
         * If the current temperature is higher than the target, send a HIGH signal to the Relay to turn on the AC.
         * If it's lower, send a LOW signal to turn off the AC.
         * Print the current status to the Serial Monitor for debugging.
         * Add a `delay` to wait a few seconds before reading again.
 4. Compile and Upload: The code is compiled and the resulting binary is uploaded to the ESP32 via a USB cable.
 5. Testing and Debugging: The engineer monitors the output on the Serial Monitor. They might use an Oscilloscope to check the signals on the pins. They warm the sensor with their hand to see if the Relay clicks on correctly.

## 7. Common Job Roles

* Kernel Developer
* Systems Engineer
* Embedded Software Engineer
* Firmware Engineer
* Robotics Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Arduino`** | An open-source electronics platform based on easy-to-program microcontrollers. |
| **`BIOS`** | Basic Input/Output System, the first program that runs when a computer is turned on. |
| **`Bootloader`** | A small program responsible for loading the OS kernel into memory. |
| **`Concurrency`** | The ability to manage multiple tasks in the same period of time. |
| **`Context Switch`** | The process of saving the state of a process and running another process on the CPU. |
| **`Driver`** | An intermediary program that allows the OS to communicate with a piece of hardware. |
| **`Firmware`** | Software permanently stored on a memory chip in a device. |
| **`GPIO`** | General-Purpose Input/Output pins on microcontrollers. |
| **`I2C`** | A popular serial communication protocol between integrated circuits. |
| **`Interrupt`** | A signal from hardware to the processor requesting immediate attention. |
| **`Kernel`** | The central part of an operating system. |
| **`Microcontroller (MCU)`** | A small, integrated computer on a single chip. |
| **`Process`** | A program in execution. |
| **`Raspberry Pi`** | A small single-board computer that often runs Linux. |
| **`RTOS`** | Real-Time Operating System, guarantees responses within specific time constraints. |
| **`Scheduler`** | The part of the kernel that decides which process to run next. |
| **`Semaphore`** | A variable used to control access to a shared resource between multiple processes. |
| **`Shell`** | The command-line interface for interacting with the operating system. |
| **`System Call`** | The way programs request a service from the kernel. |
| **`Thread`** | The smallest unit of execution within a process. |
| **`UART`** | Universal Asynchronous Receiver-Transmitter, a serial communication protocol. |
| **`Virtual Memory`** | A technique that uses the hard disk as an extension of RAM. |

</details>

[⬆️ Back to Table of Contents](README.md)

