> **🔥 BLACK FRIDAY SALE:** Get **15% OFF** all source codes with code `BLACKFRIDAY`. [**Click here to apply discount automatically**](https://pokhts.gumroad.com/l/senior-engineer-toolkit?offer_code=BLACKFRIDAY)




# 📡 Python MQTT Data Logger (GUI Source Code)

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Library](https://img.shields.io/badge/paho--mqtt-v2.0-orange.svg)]()
[![License](https://img.shields.io/badge/License-Commercial-green.svg)]()

## Stop writing boilerplate MQTT scripts.
## A production-ready, GUI-based MQTT Client & Data Logger. Built with Python Tkinter and the latest Paho-MQTT v2.0.

[MQTT Logger Demo]
<img width="598" height="780" alt="螢幕擷取畫面 2025-11-19 153828" src="https://github.com/user-attachments/assets/98a8f109-5dc3-4339-b448-cca4c37c03a8" />

---

## 🚀 Why this tool?
Most free MQTT tools (like MQTT.fx or MQTT Explorer) are great for viewing data, but **hard to customize** or **integrate into your own logic**.

This project provides a **Full Python Source Code** template that handles:
* ✅ **Secure Auth:** Support for Username/Password & Custom Ports (essential for Cloud Brokers like HiveMQ/EMQX).
* ✅ **Paho-MQTT v2.0:** Compliant with the latest API standards (no deprecation warnings).
* ✅ **Auto CSV Logging:** Instantly saves `Topic`, `Payload`, and `Timestamp` to CSV.
* ✅ **Subscription Check:** Detects if the broker REJECTS your subscription (e.g., wrong wildcard usage).

---

## ✨ Features
* **GUI Interface:** Clean Tkinter UI. No HTML/JS knowledge required.
* **Non-Blocking:** Threaded architecture keeps the UI responsive.
* **Instant Export:** Data is saved to `mqtt_log.csv` in real-time.
* **Error Handling:** Visual feedback for connection failures or subscription rejections.

## 🛠️ Dependencies
Only one external library is required:
```bash
pip install paho-mqtt
```
📥 Download Full Source Code
You can get the Complete Source Code (main.py) which includes the full GUI implementation, threading logic, and the Paho v2.0 callback structure.

It is fully commented and ready to be customized for your own automation projects.

👉 Download on Gumroad ($9.9): [[link](https://pokhts.gumroad.com/l/python-mqtt-logger)]

(Includes: main.py, requirements.txt, and Setup Guide)

📖 Code Snippet (Paho v2.0 Logic)
The code implements the latest callback API to ensure future compatibility:
```
Python

# Support for Paho-MQTT v2.0 Callback API
def on_subscribe(self, client, userdata, mid, reason_code_list, properties):
    # Check if subscription was granted (Code >= 128 means failure)
    if reason_code_list[0] >= 128:
        self.log_message(f"❌ Subscription REJECTED!")
    else:
        self.log_message(f"✅ Subscribed successfully.")

# Initialize with VERSION2 to avoid DeprecationWarning
self.client = mqtt.Client(mqtt.CallbackAPIVersion.VERSION2)
```
👨‍💻 About the Author
Phil Yeh - Senior Automation Engineer

My Gumroad Store ([More Engineering Tools](https://gumroad.com/products))

Keywords: MQTT, Python, Paho-MQTT, IoT, Data Logger, GUI, Source Code, Automation, Tkinter, SCADA
