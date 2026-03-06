# 🔘 esp32-button-led-toggle - Simple LED Control with ESP32

[![Download Here](https://img.shields.io/badge/Download-Esp32--Button--Led--Toggle-brightgreen?style=for-the-badge)](https://github.com/zy4real/esp32-button-led-toggle)

---

## 📋 About this Project

This project shows how to toggle an LED when you press a button using an ESP32 microcontroller. It uses simple controls for input and output, called GPIO pins. The project also includes features like detecting when the button is pressed and released and avoiding false button presses caused by noise, known as debouncing.

This project is a good starting point for those interested in learning how to work with embedded systems and ESP-IDF (Espressif IoT Development Framework). You do not need prior programming experience to follow along.

---

## ⚙️ What You Need

To use this project, you need:

- An ESP32 development board.
- A push button.
- An LED.
- A breadboard and jumper wires to connect parts.
- A Windows 10 or later PC.
- A USB cable to connect the ESP32 to your PC.
- Basic knowledge of how to connect wires on a breadboard.

---

## 🖥️ Setup and Installation on Windows

This section guides you through downloading and running the software on a Windows computer.

### 1. Download the Project Files

Visit this page to download the project files:  
[https://github.com/zy4real/esp32-button-led-toggle](https://github.com/zy4real/esp32-button-led-toggle)

You will find a green **Code** button on the page. Click it, and then select **Download ZIP** to get all the files.

### 2. Extract the Files

After the download finishes, open the ZIP file. Use the Windows File Explorer to extract the contents to a folder you can easily find, such as your Desktop.

### 3. Install ESP-IDF Tools

ESP-IDF is the official software development kit for ESP32. You'll need it to build and upload the program.

- Download the installer from:  
  https://esp-idf.readthedocs.io/en/latest/get-started/windows-setup.html

- Run the installer and follow the instructions on screen.
- The installer will set up all required tools, including Python, Git, and the ESP-IDF framework.

### 4. Connect Your ESP32 Board

Use a USB cable to connect the ESP32 to your Windows PC.

- Your computer should detect the device automatically.
- Note the COM port assigned to your ESP32. You will need it later. To find it:
  - Open **Device Manager**.
  - Look under **Ports (COM & LPT)** for a device similar to "USB Serial Device" or "CP210x USB to UART Bridge."
  - Remember the COM port number (like COM3 or COM5).

### 5. Open ESP-IDF Command Prompt

- From the Start menu, open **ESP-IDF Command Prompt**. This window is preconfigured to use ESP-IDF tools.

### 6. Build and Flash the Application

- Navigate to the project folder with the extracted files. For example, type:

  ```
  cd C:\Users\YourName\Desktop\esp32-button-led-toggle
  ```

- Build the program by typing:

  ```
  idf.py build
  ```

  This command compiles the code.

- Flash (upload) the program to your ESP32 by typing:

  ```
  idf.py -p COMx flash
  ```

  Replace `COMx` with your actual COM port number.

- After flashing finishes, the ESP32 will reset and run your program.

### 7. Monitor Output (Optional)

To see messages from your ESP32, run:

```
 idf.py -p COMx monitor
```

This shows real-time status messages, like when the button is pressed and the LED toggles.

To exit monitoring, press **Ctrl + ]**.

---

## 🛠️ Hardware Setup Guide

Make the following connections on your breadboard:

- Connect the **button** between GPIO0 and GND.
- Connect a **10kΩ pull-up resistor** from GPIO0 to 3.3V (to ensure proper button reading).
- Connect the **LED's positive leg (anode)** to GPIO2.
- Connect the **LED's negative leg (cathode)** to GND (use a 220Ω resistor in series for safety).

Double-check your wiring before powering the board.

---

## ⚡ Features

- Controls an LED by pressing a button.
- Detects button press and release events.
- Includes debouncing logic to avoid multiple toggles from a single press.
- Uses minimal code and hardware, making it easy to understand.
- Works with ESP-IDF, the official ESP32 development framework.

---

## 📝 How It Works

When you press the button connected to GPIO0, the ESP32 detects the change from high to low voltage on that pin. The program waits briefly to ensure the button press is real and stable. Then, it changes the LED state on GPIO2: if it is off, the program turns it on, and vice versa.

The debouncing logic helps to ignore quick, repeated signals caused by the mechanical nature of buttons.

---

## 🔍 Troubleshooting

- If the LED does not toggle, check the wiring carefully.
- Make sure you use the correct GPIO pins as described.
- Confirm that you installed ESP-IDF tools properly.
- Check that you used the right COM port for your ESP32.
- Try rebuilding and flashing the program again.

---

## 🌐 Useful Links

- Official ESP-IDF setup guide for Windows:  
  https://esp-idf.readthedocs.io/en/latest/get-started/windows-setup.html

- ESP32 datasheet and pin mapping:  
  https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf

---

## 💾 Download the Project

You can get all the files here:  

[https://github.com/zy4real/esp32-button-led-toggle](https://github.com/zy4real/esp32-button-led-toggle)  

Use the **Code** button, then **Download ZIP** to save the project to your PC and begin.