# 🔐 IoT-Based Smart Door Lock System Using Arduino Uno

An Arduino-based smart door lock system that provides secure, password-based access using a keypad, servo motor, LCD display, and buzzer.

## 📌 Project Overview

The **IoT-Based Smart Door Lock System** is a password-protected electronic locking system developed using an **Arduino Uno**.

The user enters a password through a **4×4 keypad**. If the password is correct, the servo motor unlocks the door. If the password is incorrect, access is denied and the buzzer provides an alert.

The LCD displays instructions and the current system status, making the system simple and easy to operate.

## 🎯 Objectives

- Create a low-cost electronic security system.
- Provide password-based access control.
- Automate door locking and unlocking.
- Display system instructions and status using an LCD.
- Provide an alert for incorrect password attempts.

## ⚙️ Features

- 🔑 Password-based authentication
- 🔢 4×4 keypad for password entry
- 🔓 Automatic door unlocking
- 🔒 Automatic door locking
- 📺 16×2 I2C LCD display
- 🔊 Buzzer alert
- ⚡ Arduino Uno based control
- 💰 Low-cost and easy to implement

## 🛠️ Components Used

| Component | Quantity |
|---|---:|
| Arduino Uno | 1 |
| 4×4 Keypad | 1 |
| SG90 Servo Motor | 1 |
| 16×2 I2C LCD | 1 |
| Buzzer | 1 |
| Jumper Wires | As required |
| Breadboard | 1 |

## 🔌 Pin Configuration

### 4×4 Keypad

| Keypad Pin | Arduino Pin |
|---|---:|
| Row 1 | 2 |
| Row 2 | 3 |
| Row 3 | 4 |
| Row 4 | 5 |
| Column 1 | 6 |
| Column 2 | 7 |
| Column 3 | 8 |
| Column 4 | 9 |

### Other Components

| Component | Arduino Pin |
|---|---:|
| Servo Motor Signal | 10 |
| Buzzer | 11 |
| LCD | I2C |

## 🔄 How It Works

The system follows these steps:

1. The Arduino initializes the keypad, LCD, servo motor, and buzzer.
2. The LCD asks the user to enter the password.
3. The user enters the password using the 4×4 keypad.
4. The Arduino compares the entered password with the stored password.
5. If the password is correct:
   - Access is granted.
   - The servo motor unlocks the door.
   - The LCD displays the access status.
6. If the password is incorrect:
   - Access is denied.
   - The buzzer provides an alert.
   - The LCD displays an incorrect-password message.
7. After the required operation, the servo returns the door to the locked position.

## 🧠 System Flow

```text
        ┌─────────────────┐
        │   Power ON      │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Initialize      │
        │ Arduino + LCD   │
        │ Keypad + Servo  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Enter Password  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Check Password  │
        └───────┬─┬───────┘
                │ │
        Correct │ │ Incorrect
                │ │
                ▼ ▼
      ┌───────────┐ ┌────────────┐
      │ Unlock    │ │ Access     │
      │ Door      │ │ Denied     │
      └─────┬─────┘ └──────┬─────┘
            │              │
            ▼              ▼
      ┌───────────┐  ┌────────────┐
      │ LCD Status│  │Buzzer Alert│
      └───────────┘  └────────────┘
