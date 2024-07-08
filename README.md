STM32 MPU6050 Driver
This project provides a driver for the MPU6050 sensor using an STM32 microcontroller. The driver enables communication with the MPU6050 to read accelerometer and gyroscope data.

Features
Communication Protocol: I2C communication between STM32 and MPU6050.
Sensor Data Acquisition: Reads accelerometer and gyroscope data.
Configurable: Allows configuration of MPU6050 settings.
Components
STM32 Microcontroller: The main controller used for interfacing with the MPU6050.
MPU6050: A 6-axis motion tracking device that combines a 3-axis gyroscope and a 3-axis accelerometer.
Installation
Clone the repository:

git clone https://github.com/Emrecanbl/STM32-MPU6050-Driver.git

Set up the STM32 environment:

Use STM32CubeMX to configure the I2C peripheral for communication with the MPU6050.
Generate the project and open it in your preferred IDE (e.g., STM32CubeIDE).
Load the code:

Copy the driver files into your STM32 project.
Include the MPU6050 driver header in your main application file.
Initialize the MPU6050 sensor and start reading data.

Usage
Include the Driver:
#include "mpu6050.h"
Initialize the MPU6050:
MPU6050_Init();
Read Sensor Data:

MPU6050_Data data;
MPU6050_Read_All(&data);
printf("Accelerometer: X=%d, Y=%d, Z=%d\n", data.Accelerometer_X, data.Accelerometer_Y, data.Accelerometer_Z);
printf("Gyroscope: X=%d, Y=%d, Z=%d\n", data.Gyroscope_X, data.Gyroscope_Y, data.Gyroscope_Z);
Detailed Breakdown
Initialization
The MPU6050_Init function configures the MPU6050 with default settings.
Sets up I2C communication between the STM32 and MPU6050.
Reading Data
The MPU6050_Read_All function reads both accelerometer and gyroscope data from the MPU6050.
The data is stored in a structure of type MPU6050_Data.
Configuration
The MPU6050 settings can be customized by modifying the initialization function or by adding new configuration functions.
Troubleshooting
No Data Read: Ensure that the I2C connections between STM32 and MPU6050 are correct.
Initialization Failure: Verify the MPU6050 address and I2C configuration.
Contributing
Contributions are welcome! If you have any ideas, suggestions, or improvements, feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgments
Special thanks to the open-source community and the developers of the libraries and tools used in this project.

