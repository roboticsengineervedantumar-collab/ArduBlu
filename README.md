# Arduino HC-05 to MacroDroid Bridge

An Android app built with MIT App Inventor that bridges serial data from an **HC-05 Bluetooth module** directly to **MacroDroid** using Android notifications. 

Turn your Arduino sensor readings, button presses, or hardware triggers into real-world phone automations without complex Android coding.

---

## Features
* **Easy HC-05 Connection:** Quickly pair and connect to your HC-05 Bluetooth module.
* **Serial-to-Notification:** Converts incoming `Serial.print()` messages from your Arduino into instant Android notifications.
* **MacroDroid Ready:** Designed to work seamlessly with MacroDroid's *Notification Received* trigger.
* **Lightweight:** Clean, fast interface built with MIT App Inventor.

---

## Download & Installation
1. Go to the **[Releases](../../releases)** section on the right side of this page.
2. Download the latest `.apk` file to your Android phone.
3. Open the downloaded file. If prompted, tap **Settings** and enable **"Allow from this source"** (Install Unknown Apps).
4. Open the app and grant **Bluetooth / Nearby Devices** and **Notification** permissions when asked.

---

## How to Use

### 1. Arduino Setup
Connect your HC-05 module to your Arduino (`TX` to `RX`, `RX` to `TX`, `VCC` to `5V`, `GND` to `GND`) and send a simple text trigger via Serial:

```cpp
void setup() {
  Serial.begin(9600); // Default HC-05 baud rate
}

void loop() {
  // Example: Trigger an alert when a sensor/button activates
  Serial.println("MOTION_DETECTED");
  delay(5000);
}
