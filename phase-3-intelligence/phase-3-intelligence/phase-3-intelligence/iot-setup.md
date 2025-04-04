# 🌐 IoT Setup – Product Pickup Simulation

This file describes how to simulate product pickup detection using Azure IoT Hub and mock Raspberry Pi triggers.

---

## 🔌 Azure IoT Hub Setup

1. Go to [Azure Portal](https://portal.azure.com)  
2. Search for **IoT Hub** → Click **+ Create**
3. Configuration:
   - **Name:** `CashierlessIoTHub`
   - **Tier:** Free (F1)
   - **Region:** Same as ML workspace

---

## 📟 Create IoT Device

1. Open your IoT Hub → Devices → **+ New Device**
2. Device ID: `ShelfSensorSim`
3. Authentication type: **Symmetric key**
4. Copy **Primary Connection String**

---

## 🧪 Simulate Shelf Sensors (Python Script)

Use the following Python script to send pickup events:

```python
import time
from azure.iot.device import IoTHubDeviceClient, Message

conn_str = "Your-Primary-Connection-String-Here"
device_client = IoTHubDeviceClient.create_from_connection_string(conn_str)

try:
    while True:
        product_id = "SKU-1001"
        message = Message(f'{{ "product_id": "{product_id}", "action": "picked" }}')
        device_client.send_message(message)
        print("Event sent!")
        time.sleep(10)
except KeyboardInterrupt:
    print("Simulation stopped by user.")
finally:
    device_client.shutdown()
