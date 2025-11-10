# IoT Based Energy Monitoring System (Voltage & Current Simulation)

This project demonstrates a microcontroller-based energy monitoring system that measures and displays electrical parameters such as **voltage**, **current**, **power**, and **battery status**, and provides **warning alerts** during abnormal load or low power factor conditions.  
The system is simulated using **Tinkercad** and can be extended for real-time IoT monitoring applications.

---

## 🔗 Project Simulation Link (TinkerCAD)
**Simulation:** [https://www.tinkercad.com/things/iBg32Nb4i4H](https://www.tinkercad.com/things/iBg32Nb4i4H/editel)  
*(Open the link to view circuit connections and run simulation.)*

---

## 🎯 Objective
- To monitor and display real-time electrical parameters.
- To provide alerts when power consumption or power factor crosses safe limits.
- To allow user interaction through push buttons to toggle displayed parameters.
- To form a base design that can be upgraded with real sensors and IoT cloud connectivity.

---

## 🧠 System Overview
The system uses **Arduino Uno** as the processing unit.  
Two **16×2 LCD displays** are used:
- One shows voltage & current data.
- The other shows calculated wattage, power factor, and battery status.

Push buttons simulate changing conditions, and a buzzer alerts during abnormal states.

---

## 🔌 Components Used

| Component | Quantity | Description |
|---------|:--------:|-------------|
| Arduino Uno R3 | 1 | Main controller |
| LCD 16×2 Display | 2 | Displays electrical parameters |
| 250kΩ Potentiometer | 2 | Adjusts LCD contrast |
| 220Ω Resistor | 2 | Current limiting for display |
| Push Button | 1 | Used to toggle display screens |
| 1kΩ Resistor | 3 | For switch/button inputs |
| Slide Switch | 2 | Power control simulation |
| Piezo Buzzer | 1 | Generates warning alerts |

---

## 🧩 Circuit Diagram
The circuit consists of:
- LCD1 connected to Arduino digital pins 8–13.
- LCD2 connected to Arduino pins A4, 3, 4, 5, 6, 7.
- Push buttons on pin 2, A0, and A1.
- Buzzer connected to A5.
- Potentiometers for LCD contrast control.

*(Refer schematic in Tinkercad under “Schematic View”)*
  
---

## 📝 Working Principle
- Arduino continuously calculates wattage = voltage × current × power factor.
- Display screens toggle using an interrupt button.
- Additional push buttons simulate:
  - Low power factor condition
  - High power consumption condition
- When such conditions are detected, the buzzer is activated and warning messages appear on LCD.

---

## 🧱 Code
The full Arduino code is located in:  
**`/source/IOT_Energy_Monitoring.ino`** (or paste in main folder depending on repo)

---

## ▶️ How to Run (Simulation)
1. Open the TinkerCAD link.
2. Click **Start Simulation**.
3. Observe the displayed parameters.
4. Press push buttons to:
   - Change screens
   - Trigger warnings
5. Watch buzzer and LCD alerts during abnormal states.

---

## 📊 Output / Behavior

| Condition | System Response |
|----------|----------------|
| Normal load | LCD displays voltage, current, and wattage |
| High load detected | Buzzer activates + Warning message |
| Low power factor | Warning message + buzzer |
| Battery charged/low | Display updates charge status |

---

## 🚀 Future Enhancements
- Integrate **CT sensors** and **voltage dividers** for real hardware readings.
- Send data to **IoT Cloud** (Thingspeak / Blynk / Firebase).
- Add energy usage analytics and remote monitoring dashboard.

---

## 📘 Subject
**21ECO101T – Short Range Wireless Communication**

---

## 🏁 Conclusion
This project successfully demonstrates energy monitoring with dual LCD output and safety alerts.  
It provides a foundational framework for developing a smart IoT-based energy management system.
