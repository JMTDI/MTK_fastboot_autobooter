# MTK Fastboot Autobooter for macOS, Linux & Windows

This is a **user-friendly, one-file solution** to help you trigger fastboot/boot mode on many MTK (MediaTek) phones—now available for **macOS**, **Linux**, and **Windows**.

---

## 🚀 Features

- **No separate Python file needed on Mac/Linux:** The Python code is embedded directly in the `.sh` script!
- **Automatic dependency handling:** Installs `pyserial` if missing on Mac/Linux.
- **Works on all major OSes:** Use the right file for your platform.
- **USB device detection:** Watches for new serial devices and attempts to send the FASTBOOT command.
- **Clear instructions** and user prompts.
- **Windows:** Simple `.exe`—no Python or extra installs required!

---

## 📦 Download

Head to [the latest release](https://github.com/JMTDI/MTK_fastboot_autobooter/releases/tag/v1.0) and download the appropriate file for your platform:

- **macOS/Linux:** [`autobooter-Mac_Linux.sh`](https://github.com/JMTDI/MTK_fastboot_autobooter/releases/download/v1.0/autobooter-Mac_Linux.sh)
- **Windows:** [`autobooter-Windows.exe`](https://github.com/JMTDI/MTK_fastboot_autobooter/releases/download/v1.0/autobooter-Windows.exe)

---

## 🖥️ How to Use

### macOS & Linux

1. **Download:**  
   [`autobooter-Mac_Linux.sh`](https://github.com/JMTDI/MTK_fastboot_autobooter/releases/download/v1.0/autobooter-Mac_Linux.sh)

2. **Make it executable:**  
   ```sh
   chmod +x autobooter-Mac_Linux.sh
   ```

3. **Run it:**  
   ```sh
   sudo ./autobooter-Mac_Linux.sh
   ```

4. **Follow the on-screen instructions:**
    - **Power off your phone/device completely.**
    - Disconnect your phone/device from USB.
    - Press Enter when ready.
    - Connect your device to USB **while it is powered off**.
    - (If needed, repeatedly press the power button while connecting.)
    - Wait for the tool to detect and trigger fastboot.

> **Note:** macOS and Linux do **not** require additional drivers for most modern USB-to-serial chipsets.

---

### Windows

1. **Download:**  
   [`autobooter-Windows.exe`](https://github.com/JMTDI/MTK_fastboot_autobooter/releases/download/v1.0/autobooter-Windows.exe)

2. **Install MTK Drivers:**  
   [Download the latest MTK USB drivers for Windows (MTK-Driver-v5.2307.zip)](https://mtkdriver.com/wp-content/uploads/MTK-Driver-v5.2307.zip)  
   - Extract and install the drivers before running the tool.
   - This ensures your device is properly recognized!

3. **Run:**  
   Double-click the `autobooter-Windows.exe` file or run it from the Command Prompt.

4. **Instructions:**
   - **Power off your phone/device completely.**
   - Disconnect your phone/device from USB.
   - When prompted, connect the device to USB **while it is powered off**.
   - (If needed, repeatedly press the power button while connecting.)
   - The tool will scan for the correct port and send the FASTBOOT command.

---

## 🛠️ Requirements

### macOS / Linux
- **Python 3**
- **pip for Python 3**
- **pyserial** (auto-installed by the script if needed)
- **macOS or Linux**

### Windows
- **No Python or pip required**
- **Just run `autobooter-Windows.exe`**
- **MTK USB Drivers**  
  [Download here](https://mtkdriver.com/wp-content/uploads/MTK-Driver-v5.2307.zip)

---

## 💡 How it Works

- The script/exe monitors your system for new serial devices (USB modems, USB serial adapters, etc).
- When a new device appears, it sends the `FASTBOOT` command over serial at 115200 baud.
- If the device replies with `READYTOO`, it reports success.

---

## 📝 Notes

- **Drivers:**  
  - On **Windows**, you must install the [MTK USB drivers](https://mtkdriver.com/wp-content/uploads/MTK-Driver-v5.2307.zip) before running the tool.
  - On **macOS** and **Linux**, no additional drivers are needed for most USB-to-serial chipsets.
- **Root/Permissions:**  
  - Serial access may require root, especially on Linux (`sudo` recommended).
  - On Windows, run as administrator if needed.
- **If you want to build the Windows EXE yourself:**  
  - See [original sources and instructions](https://gist.github.com/plugnburn/b3b0bcfd926c48ec5373bea84ce59337) (Python + PyInstaller).

---

## ⚠️ Disclaimer

Use at your own risk! This tool is intended for advanced users, device tinkerers, and repair technicians.

---

## 🙏 Credits

- Original idea and Windows script: [plugnburn](https://gist.github.com/plugnburn/b3b0bcfd926c48ec5373bea84ce59337)
- Linux adaptation and community improvements
- Shell+Python hybrid version by [JMTDI](https://github.com/JMTDI)

---
