

# Home Safety System




## Table of Contents

1. [Contributors](#contributors)
2. [Project Description](#project-description)
3. [Getting Started](#getting-started)
    1. [Dependencies](#dependencies)
    2. [Hardware Components](#hardware-components)
    3. [Getting the Source](#getting-the-source)
        1. [Folder Structure](#folder-structure)
4. [Software Build and Deploy](#software-build-and-deploy) 
   1. [How To Run](#how-to-run)
   2. [Pin Configurations](#pin-configurations)


## Contributors
| Name | Github |
| :---:  | :---: |
|Abdelwahab Ganna|[abdelwahabganna](https://github.com/abdelwahabganna)|
|Hashem Abdelfatah|[HashemKhaled](https://github.com/HashemKhaled)|
|Omar Sheta|[omar-sheta](https://github.com/omar-sheta)|


## Project Description
This project provides a home safety system that can detect and prevent water and gas leaks. Our system is designed to provide the user with peace of mind and protect their home from potential damage caused by water and gas leaks. This system prevents the hazards resulting from water or gas leakage at home by automatically detecting the leakage and closing the source immediately upon leakage detection. Our home safety system is easy to use and can be enabled or disabled based on the user's choice. It is designed to be highly reliable and provide the user with the relief that comes from knowing that their home is protected from potential water and gas leaks. 



## Getting Started
### Hardware Components
| Component |
| :---: |
|[STM32L432KC Microcontroller](https://store.fut-electronics.com/products/nucleo-l432kc-stm32-arm-cortex-processing-board?_pos=3&_sid=48ed8e505&_ss=r)|
|[Water Detection Sensor Module](https://store.fut-electronics.com/products/water-detection-sensor-module?_pos=2&_sid=9bd405bc6&_ss=r)|
|[Natural Gas Sensor MQ135](https://store.fut-electronics.com/products/mq135-air-quality-sensor-module?_pos=1&_sid=da144352a&_ss=r)|
|[Solenoid Valve for Fluid Control](https://store.fut-electronics.com/products/gas-sensor-module-mq5-analog-digital?_pos=2&_sid=481968769&_ss=rhttps://store.fut-electronics.com/products/solenoid-valve-electric?_pos=1&_sid=e0c67411a&_ss=r)|
|[Tower Pro micro servo 9g](https://store.fut-electronics.com/products/micro-servo-motor-1-3kg-cm?_pos=1&_sid=b7886606c&_ss=r)|
|[Breadboard](https://store.fut-electronics.com/products/breadboard-840-pin?_pos=1&_sid=b99f00db3&_ss=r)|
|[Buzzer](https://store.fut-electronics.com/products/buzzer-5v?_pos=1&_sid=785747732&_ss=r)|
|[Resistors](https://store.fut-electronics.com/products/resistor-kit-1-4w-100piece?_pos=12&_sid=0ba964ddc&_ss=r)|

### Dependencies
STM32 IDE (Integrated Development Environment).

STM32 microcontroller board.

Git is installed on your system.

### Getting the Source

Git: <https://github.com/HashemKhaled/HomeSafetySystem.git>.

#### Folder Structure

- [`main.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/main.c): Main application file
- [`stm32l4xx_hal_msp.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/stm32l4xx_hal_msp.c): HAL MSP (Microcontroller Support Package) file
- [`stm32l4xx_it.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/stm32l4xx_it.c): Interrupt handler file
- [`syscalls.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/syscalls.c): System calls file
- [`sysmem.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/sysmem.c): System memory file
- [`system_stm32l4xx.c`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/system_stm32l4xx.c): STM32L4xx system initialization file
- [`README.md`](https://github.com/HashemKhaled/HomeSafetySystem/tree/main/Core/Src/README.md): Project documentation (you are here)

## Software Build and Deploy



### How To Run

Make sure you have the necessary hardware components (water sensor, gas sensor, valves) connected properly to the STM32 board.

1- Clone the repository to your local machine using Git: <https://github.com/HashemKhaled/HomeSafetySystem.git>.

2- Open the STM32 IDE and navigate to the project directory.

3- Build the project by selecting the "Build" or "Compile" option in the IDE's menu. This will compile the source code and generate the binary file.

4- Connect the STM32 board to your computer and ensure it is recognized by the IDE.

5- Load the project to the STM32 board. This will transfer the binary file to the microcontroller.

6- Power on the STM32 board and place the sensors near water or gas sources to detect any leakage. The system should detect leaks and trigger the corresponding alarms. Additionally, the valves should be controlled to close off the leaks. 

### Pin Configurations 
1. PA0-> TIM2_CH1 (conected to the servo of the water valve)
3. PA3-> ADC1_1N8  (connected with the somke sensor)
4. PA6-> GPIO_Input (Water sensor Reading (Digital_Input))
5. PB1-> GPIO_Output (LED (alarm system))
6. PB5-> GPIO_Output (Buzzer (alarm system)) 
11. PA8-> TIM1_CH1 (conected to the servo of the water valve MQ135)

Refere to <https://github.com/shalan/CSCE4301-WiKi/wiki/G3:-Home-Safety-System> for a better view of the Pin Configurations. 
