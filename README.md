# BatMan: Battery Manager for LILYGO® TTGO T-Internet-POE

**BatMan** (Battery Manager) is a project designed to monitor and report the battery status of a LILYGO® TTGO T-Internet-POE device using Simple Network Management Protocol (SNMP) over Ethernet. The LILYGO® TTGO T-Internet-POE is an ESP32-based development board with Power over Ethernet (PoE) capabilities, making it an excellent choice for networked IoT applications.

## Key Features

- **Wired Ethernet Connectivity**: Leverages the built-in Ethernet capabilities of the LILYGO® TTGO T-Internet-POE to connect to your network, providing a reliable, wired communication channel without the need for WiFi.
- **SNMP Integration**: Implements SNMP to report real-time battery voltage data to an SNMP manager, allowing integration with network management systems like PRTG, Zabbix, or any SNMP-compatible tool.
- **Continuous Monitoring**: Periodically reads battery voltage, current, and power consumption levels using the INA219 I2C Bi-Directional DC Current/Power Monitoring Sensor Module and transmits the data over the network for monitoring and alerting purposes.
- **Customizable Update Frequency**: Allows users to set the interval for SNMP updates to fit the specific needs of their deployment environment.
- **Note**: Future updates to BatMan will include additional features such as relay control and enhanced battery management capabilities. Stay tuned for more improvements!


## Getting Started

### Hardware Requirements

- LILYGO® TTGO T-Internet-POE (ESP32-based development board)
- Ethernet cable connected to a network with DHCP or a static IP setup
- Battery connected to the TTGO board for monitoring

### Software Requirements

- Arduino IDE with ESP32 board definitions installed
- `ETH` library for Ethernet support on ESP32
- `Arduino_SNMP_Manager` or similar SNMP library

### Setup Instructions

1. Clone the "BatMan" repository.
2. Open the provided Arduino sketch in the Arduino IDE.
3. Connect your LILYGO® TTGO T-Internet-POE board to your computer via USB.
4. Upload the sketch to the device.
5. Connect the device to your Ethernet network.
6. Configure your SNMP manager to receive and process SNMP traps from the BatMan device.

## How to Use

Once the BatMan firmware is uploaded and the device is connected to the network, it will begin reporting battery status to the SNMP manager at the configured intervals. The SNMP manager can then display battery voltage data, generate alerts, and trigger actions based on the reported values.

## License

BatMan is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License. For more details, please see the [LICENSE](LICENSE) file.

## Contributing

Contributions to BatMan are welcome! If you have suggestions for new features, bug fixes, or enhancements, please open an issue or submit a pull request.4


