
### **Fire Fighting Robot - Arduino Project**  

#### **Overview**  
This **Fire Fighting Robot** is an autonomous system designed to detect and extinguish fires using an Arduino-based control system. It uses flame sensors, a gas sensor, and a water pump to identify and combat fires. Additionally, the robot can send SMS alerts and make calls using a **SIM800L** module in case of fire or gas detection.  

#### **Key Features**  
- **Fire Detection**: Uses flame sensors to detect fire in different directions.  
- **Gas Detection**: Incorporates a gas sensor to detect hazardous gases.  
- **Autonomous Navigation**: Moves towards the fire source to extinguish it.  
- **Water Sprinkler Mechanism**: Uses a servo motor and a water pump to spray water over the fire.  
- **SMS & Call Alert System**: Notifies the user via SMS and calls when gas or fire is detected.  

#### **Components Used**  
1. **Arduino Uno** - Microcontroller to control the system.  
2. **Flame Sensors (Left, Right, Front)** - Detect fire presence.  
3. **Gas Sensor** - Detects gas leaks.  
4. **SIM800L GSM Module** - Sends SMS and makes calls during emergencies.  
5. **Servo Motor** - Rotates the nozzle for water spraying.  
6. **Water Pump** - Sprays water to extinguish the fire.  
7. **DC Motors & Motor Driver** - Enables movement of the robot.  

#### **Working Mechanism**  
1. **Fire & Gas Detection**  
   - The robot continuously monitors its surroundings using flame sensors.  
   - If fire is detected, it moves toward the source and activates the water pump.  
   - If gas leakage is detected, an SMS alert is sent to the user.  

2. **Navigation & Fire Extinguishing**  
   - The robot moves forward unless an obstacle (fire) is detected.  
   - If fire is detected, it stops and activates the **water pump**.  
   - The **servo motor** moves to spread water across the affected area.  

3. **Emergency Alerts**  
   - If fire is detected, the system **calls the user** for an emergency alert.  
   - If gas is detected, an **SMS notification** is sent.  

#### **Code Functionality Breakdown**  
- `setup()`: Initializes sensors, motors, and the GSM module.  
- `loop()`: Continuously checks sensor readings and controls movement.  
- `put_off_fire()`: Activates the water pump and rotates the servo to extinguish the fire.  
- `make_call()`: Dials the stored phone number for emergency alerts.  
- `send_sms()`: Sends an SMS notification when gas is detected.  

This **Fire Fighting Robot** is an efficient safety system that can be used in homes, industries, or hazardous environments to prevent fire hazards and gas leaks.
