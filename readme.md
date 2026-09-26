# 🔐 IoT-Based Smart Door Lock System Using Arduino Uno

## 📸 Project Preview

![IoT Smart Door Lock Project](images/WhatsApp%20Image%202026-09-26%20at%2010.04.01.jpg)

---

## 📌 Project Overview

The **IoT-Based Smart Door Lock System** is an Arduino-based security system designed to provide secure, password-based access to a door.

The system uses an **Arduino Uno, 4×4 keypad, servo motor, LCD display, and buzzer** to control and monitor the door locking mechanism.

The user enters a password using the keypad. If the password is correct, the servo motor unlocks the door. If the password is incorrect, access is denied and the buzzer provides an alert.

---

## 🎯 Objectives

- Create a low-cost electronic security system.
- Provide password-based door authentication.
- Automate door locking and unlocking.
- Display system instructions and status using an LCD.
- Provide an alert for incorrect password attempts.

---

## ⚙️ Key Features

- 🔑 Password-based authentication
- 🔢 4×4 keypad for password entry
- 🔓 Automatic door unlocking
- 🔒 Automatic door locking
- 📺 LCD display for instructions and status
- 🔊 Buzzer alert
- ⚡ Arduino Uno based control
- 💰 Low-cost and easy to implement

---

## 🛠️ Components Used

| Component | Quantity |
|---|---:|
| Arduino Uno | 1 |
| 4×4 Keypad | 1 |
| SG90 Servo Motor | 1 |
| 16×2 I2C LCD | 1 |
| Buzzer | 1 |
| Breadboard | 1 |
| Jumper Wires | As required |

---

## 🔄 How It Works

1. The Arduino Uno initializes the keypad, LCD, servo motor, and buzzer.
2. The LCD asks the user to enter the password.
3. The user enters the password using the keypad.
4. The Arduino checks the entered password.
5. If the password is correct, the servo motor unlocks the door.
6. The LCD displays the access status.
7. If the password is incorrect, access is denied and the buzzer provides an alert.
8. The door returns to the locked position.

---

## 🧠 System Flow

```text
          ┌───────────────┐
          │    POWER ON   │
          └───────┬───────┘
                  │
                  ▼
       ┌─────────────────────┐
       │ Initialize System   │
       │ Arduino / Keypad    │
       │ LCD / Servo / Buzzer│
       └──────────┬──────────┘
                  │
                  ▼
       ┌─────────────────────┐
       │   Enter Password    │
       └──────────┬──────────┘
                  │
                  ▼
       ┌─────────────────────┐
       │   Check Password    │
       └─────────┬───┬───────┘
                 │   │
             Correct Incorrect
                 │   │
                 ▼   ▼
        ┌──────────┐ ┌─────────────┐
        │ Unlock   │ │Access Denied│
        │ Door     │ │             │
        └────┬─────┘ └──────┬──────┘
             │              │
             ▼              ▼
        ┌──────────┐   ┌───────────┐
        │LCD Status│   │   Buzzer  │
        └──────────┘   └───────────┘
