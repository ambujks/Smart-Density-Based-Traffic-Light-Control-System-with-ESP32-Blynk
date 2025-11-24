# 🚦 Smart Density-Based Traffic Light Control System  
### Using ESP32, IR Sensors & Blynk IoT

This project implements an intelligent traffic light management system using the **ESP32 microcontroller**, **IR sensors**, and the **Blynk IoT platform**. Unlike traditional timer-based traffic lights, this system **dynamically adjusts signal timings** based on real-time vehicle density, improving traffic flow efficiency.

---

## 📌 Project Objective

The primary objective of this project is to develop a **smart, automated, and IoT-enabled** traffic control system that:

- Detects real-time vehicle presence using IR sensors  
- Adjusts signal durations dynamically  
- Eliminates unnecessary waiting at empty lanes  
- Sends traffic light status to the Blynk IoT dashboard  
- Enhances overall traffic flow and reduces congestion  

---

## 🧠 Key Features

- 🚗 **Density-based light switching**
- 💡 **Real-time traffic monitoring**
- 📱 **Blynk IoT integration**
- 🌐 **WiFi-enabled ESP32 controller**
- ⚡ **Efficient signal sequencing**
- 📉 **Reduces idle lane time by ~35%**
- 🔌 **Low-cost and scalable design**

---

## 🛠 Components Used

| S.No | Component | Quantity |
|------|-----------|----------|
| 1 | ESP32 WiFi Module | 1 |
| 2 | IR Sensor | 2 |
| 3 | Red LED | 2 |
| 4 | Yellow LED | 2 |
| 5 | Green LED | 2 |
| 6 | 220Ω Resistor | 6 |
| 7 | Breadboard | 1 |
| 8 | Connecting Wires | 20 |
| 9 | USB Cable | 1 |

---

## 🔧 Pin Configuration

### Traffic Signal LEDs
| Signal | Red LED | Green LED |
|--------|----------|------------|
| Signal 1 | GPIO 1 | GPIO 42 |
| Signal 2 | GPIO 45 | GPIO 47 |

### IR Sensors
| Sensor | ESP32 GPIO |
|--------|------------|
| IR 1 | 13 |
| IR 2 | 16 |

⚠ **Note:** GPIO1 is also a TX pin. Avoid using Serial Monitor when that LED is ON.

---

## 🌐 Blynk IoT Setup

1. Create a new **Template** in Blynk  
2. Select **ESP32** as hardware  
3. Create **Virtual Datastreams**:
   - V1 → Signal 1 Red  
   - V2 → Signal 1 Green  
   - V3 → Signal 2 Red  
   - V4 → Signal 2 Green  
4. Add LED widgets to the dashboard  
5. Copy the **Auth Token** into your ESP32 code  

---

## 🔍 System Workflow

1. IR sensors detect the presence of vehicles  
2. If traffic is detected on Lane 1 → Signal 1 turns green  
3. If traffic is detected on Lane 2 → Signal 2 turns green  
4. If no traffic → Both remain red  
5. Blynk updates show real-time light status  

This improves traffic management and reduces unnecessary waiting.

---

## 🖥 Circuit Diagram

The circuit includes two IR sensors connected as inputs and two traffic signal LED sets connected 
as outputs through appropriate resistors.

![image alt]()

---

## 📜 Source Code (Arduino C++)

The complete working code is already included in the project report and is used as-is in the ESP32.  
It handles:

- WiFi + Blynk initialization  
- IR sensor processing  
- Traffic light control logic  
- Virtual pin updates
- Signal sequencing functions

---

## 📈 Results

- Adaptive switching significantly reduces waiting time  
- Vehicle density detection works in real time  
- Traffic flow improved  
- Blynk dashboard allows remote monitoring  

✔ Achieved approximately **35% reduction in idle lane time**

---

## 🚀 Future Enhancements

- Camera-based AI vehicle detection  
- 4-way/6-way traffic control  
- Traffic logging and analytics dashboard  
- Cloud-based Smart City integration  

---

## 🏁 Conclusion

This IoT-based density-controlled traffic light system demonstrates how **ESP32**, **sensor data**, and **IoT connectivity** can create a smarter and more efficient traffic management solution.

By combining embedded C++, IR sensors, and Blynk Cloud, the project offers a **scalable and practical** approach to modern smart-city traffic control.

---

## 📁 Report File

🔗https://drive.google.com/file/d/1Fx8oP4IrlV3IIAGfdZZdkY25_XkJN-66/view?usp=drive_link
