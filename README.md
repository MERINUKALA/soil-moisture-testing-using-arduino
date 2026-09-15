# 🌱 Soil Moisture Testing and Monitoring System

## 📌 Project Overview

The **Soil Moisture Testing and Monitoring System** is an Arduino-based embedded project designed to measure the moisture level of soil in real time using a soil moisture sensor. The system helps identify whether the soil is **dry or sufficiently moist** and demonstrates the fundamentals of sensor interfacing, analog signal measurement, and threshold-based monitoring.

This project can be extended for **smart agriculture and IoT-based irrigation systems**.

---

## 🎯 Objectives

* Measure soil moisture levels in real time.
* Interface an analog soil moisture sensor with Arduino.
* Read and process sensor values using the Arduino ADC.
* Identify dry and wet soil conditions using threshold values.
* Understand real-time sensor data acquisition for agricultural applications.

---

## 🛠️ Components Required

| Component            |    Quantity |
| -------------------- | ----------: |
| Arduino Uno          |           1 |
| Soil Moisture Sensor |           1 |
| Breadboard           |           1 |
| Jumper Wires         | As required |
| USB Cable            |           1 |
| Soil Sample          |           1 |

---

## 🔌 Circuit Connections

### Soil Moisture Sensor → Arduino Uno

| Sensor Pin | Arduino Pin |
| ---------- | ----------- |
| VCC        | 5V          |
| GND        | GND         |
| AO         | A0          |

> **Note:** The project uses the **analog output (AO)** of the soil moisture sensor to obtain a variable sensor reading.

---

## ⚙️ Working Principle

1. The soil moisture sensor is inserted into the soil.
2. The sensor detects the moisture content of the soil.
3. The analog output of the sensor changes according to the moisture level.
4. Arduino reads this analog signal through **analog pin A0**.
5. The Arduino ADC converts the analog signal into a digital value.
6. The program compares the sensor reading with a predefined threshold.
7. The Serial Monitor displays the soil moisture condition in real time.

---

## 💻 Arduino Code

```cpp
const int moisturePin = A0;

int moistureValue;
int threshold = 500;

void setup() {
  Serial.begin(9600);
}

void loop() {

  moistureValue = analogRead(moisturePin);

  Serial.print("Soil Moisture Value: ");
  Serial.println(moistureValue);

  if (moistureValue > threshold) {
    Serial.println("Soil Condition: DRY");
  } 
  else {
    Serial.println("Soil Condition: WET");
  }

  Serial.println("----------------------");

  delay(1000);
}
```

---

## 🖥️ Sample Output

```text
Soil Moisture Value: 720
Soil Condition: DRY
----------------------

Soil Moisture Value: 430
Soil Condition: WET
----------------------
```

> **Important:** Sensor readings and the correct threshold can vary depending on the specific moisture sensor, soil type, and calibration. Adjust the `threshold` value based on your actual sensor readings.

---

## 🔑 Key Concepts Demonstrated

* Arduino Programming
* Embedded C
* Analog Sensor Interfacing
* ADC / Analog Input
* GPIO
* Real-Time Data Acquisition
* Threshold-Based Monitoring
* Sensor Data Processing
* Hardware Testing
* Serial Communication

---

## 🌾 Applications

* Smart Agriculture
* Soil Condition Monitoring
* Automated Irrigation Systems
* Plant Monitoring
* IoT-Based Farming
* Agricultural Sensor Networks

---

## 🚀 Future Enhancements

The project can be further improved by adding:

* ESP32/ESP8266 for IoT connectivity.
* Real-time cloud monitoring.
* Automatic water pump control.
* Relay-based irrigation control.
* Mobile/web dashboard.
* Multiple soil moisture sensors.
* Data logging and historical analysis.

---

## 📂 Repository Structure

```text
Soil-Moisture-Testing/
│
├── Soil-Moisture-Testing.ino
└── README.md
```

---

## 👩‍💻 Author

**Meri Nukala**

Electronics & Communication Engineering Student
Embedded Systems & IoT Enthusiast

🔗 **GitHub:** https://github.com/MERINUKULA

🔗 **LinkedIn:** https://www.linkedin.com/in/meri-nukala-819957306

---

## ⭐ Skills Highlighted

**Arduino | Embedded C | Sensors | ADC | Analog Interfacing | Real-Time Monitoring | IoT | Smart Agriculture**

