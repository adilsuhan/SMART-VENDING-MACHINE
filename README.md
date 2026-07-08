##  Project Overview

Traditional vending machines are often expensive and rely on cash or proprietary payment systems. This project provides a low-cost, cloud-connected alternative by integrating IoT technologies with digital payments.

Users can browse products through a web interface, make secure UPI payments, and receive the selected product automatically after payment verification. The ESP32 continuously monitors Firebase for payment updates and controls the dispensing mechanism.

---

##  Features

-  Cashless UPI Payment
-  Web-Based User Interface
-  Firebase Realtime Database
-  ESP32 Wi-Fi Connectivity
-  Real-Time Payment Verification
-  Automatic Product Dispensing
-  Servo Motor Control
-  Transaction Logging
-  Cloud Synchronization

---

##  Hardware Components

- ESP32 Development Board
- SG90 Servo Motors (3)
- L298N Motor Driver
- DC Motor
- Relay Module
- Breadboard
- Jumper Wires
- 5V Power Supply

---

##  Software & Technologies

- Arduino IDE
- ESP32
- Firebase Realtime Database
- HTML
- CSS
- JavaScript
- Firebase Hosting
- REST API
- UPI Payment Integration

---

##  System Workflow

1. User opens the web application.
2. Products are loaded from Firebase.
3. User adds items to the shopping cart.
4. Total amount is calculated.
5. A UPI QR code/link is generated.
6. User completes the payment.
7. Payment status changes to **Completed** in Firebase.
8. ESP32 detects the payment update.
9. The corresponding servo motor rotates.
10. Product is dispensed automatically.
11. Firebase updates the status to **Dispensed**.

---

## System Architecture

```
                User
                  │
                  ▼
        Web Interface (HTML)
                  │
           HTTP (JSON)
                  │
                  ▼
     Firebase Realtime Database
                  │
          HTTP (REST API)
                  │
                  ▼
               ESP32
          ┌─────┼─────┐
          │     │     │
      Servo1 Servo2 Servo3
              │
          DC Motor
```

---

## Hardware Connections

| Component | ESP32 Pin |
|-----------|-----------|
| Servo 1 | GPIO 13 |
| Servo 2 | GPIO 12 |
| Servo 3 | GPIO 14 |
| L298N IN1 | GPIO 25 |
| L298N IN2 | GPIO 26 |
| Relay IN | GPIO 33 |

---

##  Project Structure

```
Smart-Vending-Machine/
│
├── code/
│   ├── esp32_code.ino
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── images/
│   ├── architecture.png
│   ├── flowchart.png
│   ├── dashboard.png
│   └── prototype.jpg
│
├── report/
│   └── Smart_Vending_Machine_Report.pdf
│
├── README.md
├── LICENSE
└── .gitignore
```



##  Results

- Successfully displayed products from Firebase.
- Generated UPI payment links instantly.
- Verified payments in real time.
- Automatically dispensed the selected product using ESP32 and servo motors.
- Updated payment status from **Pending → Completed → Dispensed**.
- Achieved reliable, cloud-based vending automation.

---

##  Future Enhancements

- Inventory Management
- Stock Monitoring
- QR Payment Verification APIs
- Mobile Application
- Cloud Analytics Dashboard
- Admin Panel
- Digital Receipts
- Multiple Vending Slots
- Voice-Based Product Selection

---

##  Applications

- Educational Institutions
- Offices
- Smart Cafeterias
- Retail Stores
- Hospitals
- Shopping Malls
- Railway Stations
- Airports
---
