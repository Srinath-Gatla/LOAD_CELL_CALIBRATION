**Load Cell Weight Measurement System with HX711**
**Overview**
This Arduino code implements a weight measurement system using an HX711 load cell amplifier with an ESP32 microcontroller. The code appears to contain two different implementations that have been merged together.

**Hardware Components**
ESP32 microcontroller

HX711 load cell amplifier module

Load cell connected via DOUT and SCK pins

**Pin Configuration:**

DOUT pin connected to GPIO 2

SCK pin connected to GPIO 4

**Code Structure**
First Implementation (Basic Reading)
Initializes the HX711 scale with basic configuration

Uses scale.get_value(5) to get raw ADC readings averaged over 5 samples

Continuously monitors and prints readings every 500ms

Includes basic error handling for HX711 detection

Second Implementation (Calibrated Weight Measurement)
More advanced implementation with calibration factor

Uses scale.set_scale(101.9128) with a pre-calibrated value

Implements power management with scale.power_down() and scale.power_up()

Displays actual weight units using scale.get_units(10) averaged over 10 readings

Prints weight with 1 decimal place precision

**Key Features**
**Dual Implementation:** Contains both raw ADC reading and calibrated weight measurement approaches

**Calibration:** Uses a specific calibration factor (101.9128) for accurate weight conversion

**Power Management:** Implements sleep mode to reduce power consumption

**Averaging:** Uses multiple samples (5 or 10) for stable readings

**Error Handling:** Detects and reports HX711 connectivity issues

Serial Communication
**Baud rate:** 57600

Outputs either raw HX711 readings or calibrated weight values

Includes descriptive headers for better readability

**Usage**
The system is designed for weight measurement applications where precise force or weight sensing is required, typical in industrial, laboratory, or DIY projects requiring load cell integration.
