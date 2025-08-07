# Facial Recognition Gate System

A facial recognition-based security system using a Raspberry Pi and Arduino. This project uses a webcam and facial recognition software to authenticate users and, upon successful recognition, activates a servo motor to open a physical gate or lock — represented by an RGB LED and servo motor mechanism.

## 📌 Project Description

This system combines the power of the Raspberry Pi’s processing and facial recognition capabilities with the real-time control of an Arduino. A webcam connected to the Raspberry Pi captures facial data, which is processed using a facial recognition algorithm. If a recognized face is detected, the Raspberry Pi signals the Arduino to unlock the "gate" by activating a servo motor and displaying a green LED. Unrecognized faces trigger a red LED and deny access.

This project can be adapted for smart door locks, office check-ins, or other physical authentication systems.

---

## 🧰 Components Used

| Component        | Quantity | Description                                  |
|------------------|----------|----------------------------------------------|
| Arduino Uno R3   | 1        | Microcontroller for controlling the servo and LED |
| Raspberry Pi     | 1        | Handles facial recognition and decision logic |
| Webcam           | 1        | Captures facial images                        |
| Breadboard       | 1        | For prototyping and connecting components     |
| RGB LED          | 1        | Indicates access (Green = granted, Red = denied) |
| Servo Motor      | 1        | Acts as the gate mechanism                    |
| Jumper Wires     | 10      | For connecting components                     |

---

## ⚙️ Installation & Setup

### Raspberry Pi Setup

1. **Install dependencies:**
   ```bash
   sudo apt update
   sudo apt install python3-opencv python3-pip
   pip3 install face_recognition numpy
Connect the webcam via USB.

Clone the project repository:

bash
Copy
Edit
git clone https://github.com/yourusername/facial-recognition-gate.git
cd facial-recognition-gate
Run the facial recognition script:

bash
Copy
Edit
python3 facial_recognition.py
This script communicates with the Arduino via serial (USB).

## Arduino Setup
Upload the Arduino sketch:

Open facial_gate.ino in the Arduino IDE.

Select the correct board and port.

Upload the code.

Wiring:

Servo Signal Pin → Digital Pin 9

RGB LED:

Red → Pin 3

Green → Pin 5

Blue → Pin 6

Ground all components to Arduino GND.

## 🧠 How It Works
The webcam captures a live video stream.

The Raspberry Pi runs facial recognition using the face_recognition Python library.

When a known face is detected:

A signal is sent to the Arduino via USB serial.

The Arduino activates the servo motor, opening the "gate".

The RGB LED turns green.

If the face is unrecognized:

The servo remains closed.

The RGB LED turns red.

## 📸 Images / Demo Videos
Media Type	Description
Breadboard + Arduino + Servo layout
Gate unlocking upon face recognition
▶️ Watch Demo Video	Full system in action(https://drive.google.com/file/d/1vR2NGlbOfV1yIlDdnlDzg5l_BcO_kL0i/view)

## 🔗 Simulation Links
Simulations may be limited due to hardware dependencies, but you can simulate the Arduino portion using Tinkercad.

Arduino Servo + LED Simulation

## 🙌 Credits
Project Developer: Jaden Chapman

**Libraries Used**:
face_recognition
OpenCV for video processing

**Special Thanks**:
OpenAI ChatGPT for README assistance
Raspberry Pi Foundation & Arduino Community

