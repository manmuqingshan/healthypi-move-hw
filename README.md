<div align="center">
  
![HealthyPi Move Logo](/docs/images/healthypi_move_logo.png)

</div>

# HealthyPi Move Hardware Repository

**An open-source biometric monitor in a watch form factor**

HealthyPi Move is a revolutionary open-source wearable device that provides clinical-grade biometric monitoring in a sleek watch form factor. Designed with the principles of data ownership, repairability, and customization at its core, HealthyPi Move offers comprehensive health tracking capabilities without the limitations of proprietary systems.

![HealthyPi Move](/docs/images/healthypi-move.jpg)

## Project Status

** Successfully Funded & Shipping!** - HealthyPi Move reached 329% of its funding goal on Crowd Supply and is now shipping to backers worldwide.

- **Campaign Status**: Funded and In Stock
- **Availability**: Shipping now - [Order on Crowd Supply](https://www.crowdsupply.com/protocentral/healthypi-move)
- **Price**: $299 USD

## Key Features

### Comprehensive Biometric Monitoring
- **ECG (Electrocardiogram)**: Single-lead ECG for heart rhythm analysis
- **Dual PPG Sensors**: Wrist and finger-based photoplethysmography
- **SpO₂ Monitoring**: Blood oxygen saturation measurement
- **Blood Pressure Trending**: Cuffless BP monitoring via finger sensor
- **EDA/GSR**: Galvanic skin response for stress monitoring
- **Heart Rate Variability (HRV)**: Advanced cardiac health metrics
- **Respiration Rate**: ECG-derived breathing pattern analysis
- **Body Temperature**: Contact-based temperature sensing
- **Activity Tracking**: 6-axis IMU for motion and activity monitoring

### Technical Specifications
- **Processor**: Nordic nRF5340 dual-core ARM Cortex-M33 SoC
- **Memory**: 512 KB RAM, 128 MB QSPI flash storage
- **Display**: 1.2" round AMOLED (390×390 pixels) with capacitive touch
- **Battery**: 300 mAh Li-Po with 5-day typical usage life
- **Connectivity**: Bluetooth Low Energy 6.0, USB Type-C
- **Charging**: USB Type-C with Power Delivery support
- **Dimensions**: 43mm diameter × 13mm thickness
- **Strap Compatibility**: Standard 22mm watch straps

### Open Source Advantages
- **Own Your Data**: No cloud dependency, all data stored locally
- **User Programmable**: Based on Zephyr RTOS and nRF Connect SDK
- **Repairable Design**: Modular components, no glue assembly
- **Custom Applications**: Full access to develop your own algorithms
- **OTA Updates**: Over-the-air firmware updates via BLE or USB

## Repository Contents

### Hardware Design Files
* **`/pcbs/main board/`** - Main board PCB designs (KiCad and Eagle formats)
  * Latest: `kicad_pc_healthypi_move_nRF5340_v12/` (KiCad)
  * Legacy versions: v1-v5 (Eagle format)
* **`/pcbs/sensor board/`** - Sensor board PCB designs
  * Latest: `kicad_pc_healthypi_move_sensor_v9/`
* **`/pcbs/finger sensor board/`** - Finger sensor PCB designs
  * Latest: `pc_healthypi_move_sensor_connector_v4/`
* **`/pcbs/bottom board/`** - Bottom board PCB designs
  * Latest: `pc_healthypi_move_bottom_pcb_v4/`
* **`/enclosure/`** - 3D printable and injection-molded enclosure designs
  * **`/enclosure/fusion/`** - Autodesk Fusion 360 source files
  * **`/enclosure/stls/`** - 3D printable STL files
* **`/docs/`** - Documentation and images

## Related Repositories

- **[HealthyPi Move Firmware](https://github.com/Protocentral/healthypi-move-fw)** - Zephyr RTOS-based firmware
- **[HealthyPi Move Mobile App](https://github.com/Protocentral/healthypi_move_flutter/)** - Flutter-based companion app (Android/iOS)

## Sensor Details

### ECG (Electrocardiogram)
- **IC**: MAX30001 ECG and bio-impedance front-end
- **Configuration**: Single-lead ECG (Lead-II equivalent)
- **Electrodes**: Back electrode (wrist contact) + top bezel electrode (finger contact)
- **Sampling Rate**: Up to 512 Hz
- **Features**: Real-time heart rate, HRV calculation, respiration rate derivation

### PPG (Photoplethysmography) - Dual Configuration
#### Wrist PPG Sensor
- **IC**: MAX86141 with MAX32664C biometric sensor hub
- **LEDs**: 2× Green, 1× Red, 1× Infrared
- **Photodiodes**: 2× photodiodes for improved signal quality
- **Use Cases**: Continuous HR monitoring, SpO₂ measurement

#### Finger PPG Sensor (Optional)
- **IC**: MAX30101 with MAX32664D biometric sensor hub
- **LEDs**: Red and Infrared
- **Use Cases**: High-accuracy SpO₂, blood pressure trending, pulse transit time
- **Connection**: USB Type-C port with custom connector board

### Additional Sensors
- **IMU**: BMI323 6-DoF (accelerometer + gyroscope)
- **Temperature**: MAX30208 body temperature sensor
- **EDA/GSR**: Custom electrodes for galvanic skin response

## Enclosure Design

The HealthyPi Move features a thoughtfully designed enclosure that prioritizes repairability and modularity:

### Key Design Principles
- **Screw Assembly**: No glue used - completely serviceable
- **Modular Construction**: Separate main board, sensor board, and battery modules
- **Standard Straps**: Compatible with any 22mm watch strap
- **Material**: Biocompatible ABS-type injection-molded plastic

### Chassis System
- **4-Screw Design**: Easy access to internal components
- **Component Protection**: Isolated battery compartment for safety
- **Display Replacement**: User-replaceable AMOLED display
- **Sensor Access**: Removable sensor boards for upgrades/repairs

## Applications & Use Cases

### Personal Health Monitoring
- **Continuous Monitoring**: 24/7 heart rate, activity, and sleep tracking
- **Stress Management**: Real-time EDA/GSR feedback for stress awareness
- **Cardiovascular Health**: ECG recording and HRV analysis
- **Fitness Tracking**: Advanced metrics beyond basic step counting

### Research & Development
- **Clinical Research**: IRB-approved studies with institutional oversight
- **Algorithm Development**: Platform for custom biometric algorithms
- **Data Collection**: High-resolution, multi-modal biometric datasets
- **Educational Use**: Teaching platform for biomedical engineering

### Healthcare Applications*
- **Remote Monitoring**: Patient monitoring with healthcare provider integration
- **Chronic Disease Management**: Long-term tracking for conditions like AFib
- **Telehealth Integration**: Data export for virtual consultations
- **Clinical Trials**: Research-grade data collection platform

*_Requires appropriate regulatory approvals (FDA, CE, etc.) for medical use_

## 🛠️ Development Environment

### Firmware Development
- **OS**: Zephyr RTOS with nRF Connect SDK
- **Language**: C/C++
- **IDE**: VS Code with nRF Connect extension
- **Debugging**: SWD via USB Type-C DAM
- **OTA Updates**: BLE and USB DFU support

### Mobile App Development
- **Framework**: Flutter (Dart)
- **Platforms**: Android, iOS, macOS, Windows, Linux
- **Communication**: Bluetooth Low Energy
- **Data Format**: JSON, CSV, PDF export capabilities

### Hardware Customization
- **PCB Design**: KiCad (latest versions) and Eagle (legacy)
- **Enclosure**: Autodesk Fusion 360 source files
- **3D Printing**: STL files provided for rapid prototyping
- **Manufacturing**: Gerber files and assembly documentation included

## 📚 Documentation & Support

Visit our [Documentation Site](https://move.protocentral.com/) for detailed guides.

## ⚖️ Regulatory Information

### Important Disclaimers
⚠️ **Medical Device Notice**: HealthyPi Move is **NOT** a certified medical device. It is designed for:
- Consumer wellness and fitness tracking
- Research and educational applications
- Development of medical devices (with proper certification)

## 📄 License Information

![License](license_mark.svg)

This project is open source and licensed under multiple licenses depending on the component:

### Hardware
**All hardware designs are released under the [CERN-OHL-P v2](https://ohwr.org/cern_ohl_p_v2.txt)** license.

Copyright CERN 2020. This source describes Open Hardware and is licensed under the CERN-OHL-P v2. You may redistribute and modify this documentation and make products using it under the terms of the CERN-OHL-P v2 (https://cern.ch/cern-ohl). This documentation is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE.

### Software
**All software is released under the [MIT License](http://opensource.org/licenses/MIT).**

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Documentation
**All documentation is released under [Creative Commons Share-alike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/).**

![CC-BY-SA-4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original

Please check [*LICENSE.md*](LICENSE.md) for detailed license descriptions.

