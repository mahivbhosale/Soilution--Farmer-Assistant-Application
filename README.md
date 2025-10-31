# 🌱 Soilutions – Smart Soil Moisture Monitoring and Irrigation Recommendation System

## 📘 Overview
**Soilutions** is an IoT-based smart agriculture solution designed to assist farmers in monitoring soil moisture levels in real-time and receiving recommendations for optimal water usage based on soil type and crop selection.

The system integrates an **ESP32 microcontroller**, **Soil Moisture Sensor**, and a **Flutter mobile application** to provide seamless data visualization and intelligent irrigation suggestions.

---

## 🎯 Objectives
- To monitor soil moisture levels using sensors connected to ESP32.
- To display real-time sensor data on a mobile app.
- To recommend irrigation levels based on predefined datasets.
- To improve water management and support sustainable agriculture.
- To serve as a base for future AI/ML integration in smart farming.

---

## ⚙️ System Architecture
The project follows this flow:

1. **Data Collection (IoT Layer):**
   - The **Soil Moisture Sensor** connected to **ESP32-WROOM-32** reads the real-time soil moisture.
   - Data is processed and transmitted via Wi-Fi.

2. **Data Transmission:**
   - The ESP32 sends sensor readings to the Flutter app over Wi-Fi using an HTTP endpoint.

3. **Application Layer (Flutter App):**
   - The app displays live soil moisture percentage.
   - The user inputs **crop** and **soil type**.
   - The app compares real-time data with an internal dataset (`dataset.csv`) and provides water recommendations.

4. **Recommendation Layer:**
   - The app uses dataset mapping to recommend optimal water levels for each crop-soil combination.

---

## 📱 Screenshots
Below are sample screenshots from the Soilutions mobile app:

| Live Data | Crop & Soil Input | Water Recommendation | Dashboard |
|------------|------------------|----------------------|------------|
| ![Live Data](assets/screenshots/app1.jpg) | ![ESP](assets/screenshots/app2.jpg) | ![Recommendation](assets/screenshots/app3.jpg) | 

> *(You can place your images inside `assets/screenshots/` folder and rename them accordingly.)*

---

## 🧩 Components Used
### Hardware
- ESP32-WROOM-32 Microcontroller  
- Soil Moisture Sensor  
- Breadboard and Jumper Wires  

### Software
- Flutter SDK (for Mobile App)
- Arduino IDE (for ESP32)
- Dataset (`dataset.csv`) for crop-soil moisture mapping

---

## 🧠 Future Scope
- Integration of **Machine Learning** models (like XGBoost or Decision Tree) to predict irrigation needs based on environmental and historical data.
- Support for **multiple sensors** (temperature, humidity, pH).
- Integration with **cloud storage** and analytics dashboards.
- **Offline-first mobile app** with synchronization once connected.

---

## 🛠️ Setup and Installation
### ESP32 Setup
1. Open `final_ip.ino` in Arduino IDE.  
2. Install the **ESP32 board package** and select the correct board (ESP32-WROOM-32).  
3. Connect the soil moisture sensor to analog pin **GPIO34**.  
4. Upload the code and check serial output.

### Flutter App Setup
1. Open the Flutter project folder in Android Studio or VS Code.  
2. Run `flutter pub get` to install dependencies.  
3. Connect your mobile or use an emulator.  
4. Run `flutter run` to launch the app.  

---

## 🧾 Dataset Information
The file **`dataset.csv`** contains predefined optimal soil moisture values for different crops and soil types.

| Crop | Soil Type | Ideal Moisture (%) |
|------|------------|--------------------|
| Wheat | Loamy | 45 |
| Rice | Clay | 60 |
| Maize | Sandy | 35 |

---

## 👥 Team Members
- **Shubham Goni**  
- *(Add other team members here if applicable)*

---

## 📚 Conclusion
The Soilutions project successfully demonstrates the use of IoT and mobile technology for smart agriculture. It enables real-time monitoring, decision-making assistance, and paves the way for integrating machine learning for more intelligent and automated irrigation systems.

---

## 🧑‍💻 Repository Structure
```
Soilutions/
├── ESP32/
│   └── final_ip.ino
├── Flutter_App/
│   ├── lib/
│   ├── android/
│   ├── ios/
│   └── pubspec.yaml
├── dataset/
│   └── dataset.csv
├── assets/
│   └── screenshots/
├── README.md
└── .gitignore
```

---

## 🪄 License
This project is developed for educational and research purposes. Feel free to modify and extend it for learning or personal use.
