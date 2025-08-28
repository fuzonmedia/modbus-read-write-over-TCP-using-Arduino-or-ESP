# Arduino Modbus TCP Client (Ethernet)

This project demonstrates how to use an **Arduino MKR board with MKR ETH Shield** as a **Modbus TCP Client**.  
It connects to a Modbus TCP Server over Ethernet and performs **coil write** and **holding register read** operations for sensors like **Temperature & Humidity (T&H)**, **CO₂ sensors**, and **Energy Meters (L&T Wh)**.

---

## ✨ Features
- 📡 Implements **Modbus TCP client** over Ethernet  
- 🔗 Connects to any Modbus TCP server (port 502)  
- 🖊️ Supports **coil write** operations  
- 📖 Reads holding registers (16-bit / float)  
- 🏭 Tested with **industrial Modbus TCP devices**

---

## 🔧 Hardware Required
- Arduino MKR Board (e.g., MKR Zero, MKR WiFi 1010)  
- MKR ETH Shield  
- Ethernet cable + Local Modbus TCP server device (PLC, Energy meter, Simulator)

---

## 📡 Network Configuration
Update your board’s network details in the sketch:

```cpp
byte mac[] = { 0xDE, 0xAD, 0xBE, 0xEF, 0xFE, 0xED };
IPAddress ip(192, 168, 33, 65);
IPAddress gateway(192, 168, 33, 1);
IPAddress subnet(255, 255, 255, 0);
IPAddress server(192, 168, 33, 60);  // Modbus server IP
