

# Home Safety System

## Group Members
| Name | Github |
| :---:  | :---: |
|Abdelwahab Ganna|[abdelwahabganna](https://github.com/abdelwahabganna)|
|Hashem Abdelfatah|[HashemKhaled](https://github.com/HashemKhaled)|
|Omar Sheta|[omar-sheta](https://github.com/omar-sheta)|


## The Proposal
This project provides a home safety system that can detect and prevent water and gas leaks. Our system is designed to provide the user with peace of mind and protect their home from potential damage caused by water and gas leaks. This system prevents the hazards resulting from water or gas leakage at home by automatically detecting the leakage and closing the source immediately upon leakage detection. Our home safety system is easy to use and can be enabled or disabled based on the user's choice. It is designed to be highly reliable and provide the user with the relief that comes from knowing that their home is protected from potential water and gas leaks. 

## Design

<img src="https://user-images.githubusercontent.com/64085426/235797265-2dd67081-a4e0-43f4-bb36-a699c6374e5e.jpeg" width="50%">

## Identified Components
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

## How it works

**Water Leak Detection:** The Water Detection Sensor Module is placed in areas prone to water leaks, such as near sinks, washing machines, or pipes. When the sensor detects the presence of water, it sends a signal to the microcontroller.

**Gas Leak Detection:** The Natural Gas Sensor MQ5 is utilized to detect gas leaks within the home. It can detect various gases, including natural gas. Once a gas leak is detected, the sensor sends a signal to the microcontroller. However, in testing we use MQ135 which basically has the same connections but detects Co2 instead of Gas just for debugging.

**Microcontroller Processing:** The STM32L432KC microcontroller receives the signals from the water and gas sensors. It processes the signals and determines the appropriate actions to be taken based on the detected leak type.

**Closing Solenoid Valve:** If a water or a gas leak is detected, the microcontroller triggers the Solenoid Valve, which shuts off the supply to prevent further leakage.

**Servo micro:** acts as a place holder for the Solenoid Valve as it was not available.  

**Alert System:** In case of either a water or gas leak, the Buzzer is activated to generate an audible alert, notifying the inhabitants of the potential hazard. 


## Flow chart

<img src="https://github.com/shalan/CSCE4301-WiKi/assets/70941685/23ae8a1c-024a-4b6d-bfb6-c00ad34be29c" width="50%">


## Timeline

### Water Sensor in action

We developed a working initial prototype of the water sensor and valve As can be seen from the attached Images:

The First Image is of the system with no water and we see that the system is off.

<img src="https://github.com/shalan/CSCE4301-WiKi/assets/70941685/fd6999d5-a00e-4d7a-90ec-04f633ae93cc" width="50%">

The second Image is of introducing water to the system but still the system did not get into contact with it:

<img src="https://github.com/shalan/CSCE4301-WiKi/assets/70941685/2133e967-d95d-4280-ab2d-eefd5eddbe55" width="50%">

The Third Image is when the sensor gets in contact with water and the led is turned on indicating that the sensor is active. Finally the Tower Pro micro starts turning indicating closing the valve. 

<img src="https://github.com/shalan/CSCE4301-WiKi/assets/70941685/de16c550-728b-42fe-838f-075b538509d8" width="50%">

### Gas Sensor in action

The Gas sensor for the sake of prototyping was replaced by an MQ-135 sensor to detect the CO2 level by converting the adc value measured from its analog output to CO2 concetration level in part per milion (ppm) using the calibration procedure provided in the sensor's datasheet.

<img src="https://github.com/HashemKhaled/HomeSafetySystem/assets/64085426/46485f85-8e2a-4a9a-8614-40a348ce5a9e" width="50%">

### Demo for the Final Version of the System

The system now consists of a water sensor, MQ-135 sensor, alarm system (a LED and a buzzer), and two micro servo SG90 to control: one for controlling the water leakage and the other for controlling the gas leakage. 

[Link to Demo Video](https://www.youtube.com/watch?v=5CNIbkUylho&ab_channel=HashemElmalih)

## Software Build and Deploy Instructions

### Prerequisites:

STM32 IDE (Integrated Development Environment).
STM32 microcontroller board.
Git is installed on your system.
Make sure you have the necessary hardware components (water sensor, gas sensor, valves) connected properly to the STM32 board.

1- Clone the repository to your local machine using Git: <https://github.com/HashemKhaled/HomeSafetySystem.git>
Open the STM32 IDE and navigate to the project directory.

2- Open the STM32 IDE and navigate to the project directory.

3- Build the project by selecting the "Build" or "Compile" option in the IDE's menu. This will compile the source code and generate the binary file.

4- Connect the STM32 board to your computer and ensure it is recognized by the IDE.

5- Load the project to the STM32 board. This will transfer the binary file to the microcontroller.

7- Power on the STM32 board and place the sensors near water or gas sources to detect any leakage. The system should detect leaks and trigger the corresponding alarms. Additionally, the valves should be controlled to close off the leaks. 


