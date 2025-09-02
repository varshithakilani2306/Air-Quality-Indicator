# Air Quality Indicator

## Abstract
The Air Quality Indicator project is designed to monitor air pollution levels in real-time using an Arduino-based system integrated with an MQ135 gas sensor. The system captures the concentration of harmful gases such as carbon dioxide (CO2), ammonia (NH3), nitrogen oxides (NOx), alcohol, benzene, and smoke. The air quality is presented on an LCD screen in parts per million (PPM), and warnings are triggered through a buzzer and LED indicators when pollution levels exceed safe thresholds. This system aims to provide environmental awareness and real-time pollution data for better health and safety management. It also supports alerts via notification messages for immediate action.

## Methodology

### Components Used
- **Arduino Uno**: Microcontroller for processing sensor data.  
- **MQ135 Gas Sensor**: Detects harmful gases and provides output voltage proportional to gas concentration.  
- **DHT-22 Sensor**: Measures temperature and humidity (optional depending on implementation).  
- **LCD Display**: Displays real-time air quality in PPM.  
- **Buzzer & LEDs**: Provide audio-visual indication of air quality status.  
- **GSM Module (optional)**: Sends alerts via SMS.  
- **Cloud Storage & Web Server (optional)**: For remote monitoring through IoT.

### Project Phases (Based on RAD Model)
- **Requirements Planning**  
  - Define objectives: Real-time air quality monitoring with alerting capability.  
  - Identify sensors and hardware for data capture and processing.  
  
- **User Design**  
  - Develop prototype integrating sensors, microcontroller, LCD, buzzer, LEDs.  
  - Design user interface on LCD and optional web app for IoT monitoring.  
  
- **Construction**  
  - Assemble hardware: Connect MQ135 sensor to Arduino analog input.  
  - Write code for data reading, conversion of sensor analog voltage to PPM.  
  - Implement thresholds for triggering buzzer and LED alerts.  
  - Integrate optional GSM for SMS alerts and IoT cloud platform for remote access.  
  
- **Testing and Cutover**  
  - Test system in various environments.  
  - Validate sensor accuracy and alert reliability.  
  - Fine-tune threshold values and software stability.

### Working Principle
- MQ135 sensor outputs an analog voltage based on the concentration of gases.  
- Arduino reads this voltage and converts it to PPM using calibration algorithms.  
- Air quality status ("Good" or "High") is displayed on the LCD with PPM values.  
- If pollution level crosses the threshold:  
  - Buzzer sounds.  
  - Red LED lights up.  
  - Alert messages sent via GSM or IoT platform.  
- If air quality improves:  
  - Buzzer silences.  
  - Green LED lights.  
  - Display shows "Fresh Air".

## Sample Diagrams for Readme

### Block Diagram of the System
- MQ135 Sensor connected to Arduino Analog Pin.  
- Arduino connected to LCD Display and Buzzer.  
- LEDs connected to Arduino digital pins.  
- (Optional) GSM module connected for SMS alert.  
- (Optional) Wi-Fi module or Raspberry Pi for IoT and cloud integration.

### Flowchart of System Working
Start → Initialize sensors and components → Read air quality data → Convert voltage to PPM → Is PPM > Threshold?
↓ ↓
Yes → Turn ON Buzzer & Red LED → Display "AQ Level High" → Send Alert
No → Turn OFF Buzzer & Red LED → Turn ON Green LED → Display "AQ Level Good"
↓
Loop


## Results
- Successfully displays real-time air quality in PPM on LCD.  
- Buzzer and LED alerts effectively notify when pollution goes beyond safe limits.  
- System capable of capturing air pollution data remotely if combined with IoT/cloud.  
- Can be implemented for indoor and outdoor air quality monitoring.

## Conclusion
This Arduino-based Air Quality Indicator provides an efficient, low-cost solution for real-time monitoring of air pollution. It effectively detects multiple harmful gases and alerts users when pollution exceeds safety thresholds. The system can be extended with IoT technologies for remote monitoring and data logging, supporting proactive environmental management and public health safety.

