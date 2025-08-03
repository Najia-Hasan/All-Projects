# Responsive Tic Tac Toe Game

A minimal, dark-themed, responsive Tic Tac Toe game built using HTML, CSS, and JavaScript. It features subtle animations, pop-up winner announcements, and smooth UX.

## 🎮 Features
- Fully responsive layout
- Animated box effects
- Pop-up winner display
- Reset button to restart game

##  Files Included
- `index.html` – Game layout and structure
- `style.css` – Dark mode theme and animations
- `script.js` – Game logic and interactions

##  Demo
> Play the game in your browser by opening `index.html`.

##  Learning Goals
- JavaScript game logic
- Responsive and animated UI
- Event handling and DOM manipulation

## Url
https://tic-tac-toe-bynajia.netlify.app

---

## 🚀 Subway Runner – Endless Runner Game

Subway Runner is a fun and engaging endless runner game inspired by **Subway Surfers**, developed using **HTML5**, **CSS3**, and **JavaScript** (Canvas API). The player controls a runner to avoid obstacles and collect coins in an infinite, fast-paced environment with an animated background.

---

## 🎮 Features

- 🎯 Full-screen gameplay (`2500x800` canvas)
- 🧍 Smooth player movement with keyboard controls
- 🧱 Obstacles that spawn randomly across the screen
- 🪙 Collect coins and increase your score
- 🌆 Animated, scrolling background
- ⚠️ Collision detection and game-over logic
- ✨ Clean UI and custom graphics

---

## 🔧 Tech Stack

- **HTML5** – Canvas for rendering graphics
- **CSS3** – Styling, layout, shadows
- **JavaScript** – Game logic, animations, and user input handling

---
# Car Showcase Landing Page

A sleek and simple landing page to display car details or advertisements. Perfect for auto businesses or as a design prototype.

## 🚗 Highlights
- Clean layout with inline CSS
- Responsive design structure
- Ideal for showcasing a single or multiple vehicles

##  Contents
- `car.html` – The main landing page with embedded styling

##  Use Case
- Car dealership landing page
- Portfolio template for automotive designers
- Educational HTML/CSS practice

##  Skills Used
- HTML page structuring
- Inline CSS styling
- Visual layout design
- 
## Url
https://subway-runner.netlify.app

---
# Warm Fashion - Winter Wear Landing Page

A stylish and warm-themed landing page for fashion brands or e-commerce seasonal campaigns. Built using basic HTML and CSS.

## 👗 Key Features
- Winter-inspired design
- Product and brand focus
- Clean layout with good color contrast
- Optimized for simple branding pages

##  Files Included
- `index.html` – Page layout and content
- `style.css` – Styling for a cozy, aesthetic appearance

##  Ideal For
- Fashion portfolio showcase
- Online store mockup
- HTML/CSS learning projects

##  Technologies Used
- HTML5
- CSS3

---

# 📡 RFID-Based Smart System

This project demonstrates the use of **Radio Frequency Identification (RFID)** technology to build a smart, contactless identification or access control system. The system is designed using an **RFID reader module**, integrated with **Arduino** or a microcontroller, and optionally connected to a database or web interface for logging and control.

---

## 🎯 Project Objective

To build a secure and efficient **RFID-based system** for:
- 📋 Attendance management
- 🔐 Access control (e.g., doors, labs, lockers)
- 🏷️ Inventory or asset tracking

---

## 🛠️ Features

- 🔄 Real-time RFID card scanning and identification
- 🔒 Secure access via unique RFID tags
- 💾 Optional data logging (to serial monitor or database)
- 🟢 Visual/audio feedback (LEDs, buzzer, display)
- 🧩 Easy to integrate with web or desktop applications

---

## 🧰 Components Used

| Component        | Description                          |
|------------------|--------------------------------------|
| 🔘 Arduino Uno/Nano | Microcontroller board               |
| 🪪 RFID RC522      | RFID Reader Module                  |
| 🏷️ RFID Tags/Cards | Unique identifiers (13.56 MHz)     |
| 🔊 Buzzer / LED    | Feedback for access success/failure |
| 🖥️ Optional Display| LCD/OLED to show user info          |
| 🧠 Optional Server | For logging user entries (PHP/MySQL or Firebase) |

---

## 🔌 Circuit Diagram

> *(Insert your Fritzing circuit diagram here or describe the pin connections)*

- SDA → D10  
- SCK → D13  
- MOSI → D11  
- MISO → D12  
- RST → D9  
- GND → GND  
- VCC → 3.3V

---

## 👨‍💻 Code Snippet (Arduino Example)

```cpp
#include <SPI.h>
#include <MFRC522.h>

#define SS_PIN 10
#define RST_PIN 9

MFRC522 rfid(SS_PIN, RST_PIN);

void setup() {
  Serial.begin(9600);
  SPI.begin();
  rfid.PCD_Init();
  Serial.println("Scan RFID Card...");
}

void loop() {
  if (!rfid.PICC_IsNewCardPresent() || !rfid.PICC_ReadCardSerial()) return;

  Serial.print("UID Tag: ");
  for (byte i = 0; i < rfid.uid.size; i++) {
    Serial.print(rfid.uid.uidByte[i] < 0x10 ? " 0" : " ");
    Serial.print(rfid.uid.uidByte[i], HEX);
  }
  Serial.println();

  delay(1000);
}
---



