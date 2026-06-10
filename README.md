# VRChat Speech-To-Text Chatbox Controller

An open-source accessibility and quality-of-life tool for VRChat that converts your spoken voice into real-time text inside the game's chatbox. Powered by **Vosk** for offline, private voice recognition and **python-osc** to communicate seamlessly with VRChat.

## Features
* **100% Offline & Private:** No cloud API keys required. Your voice data never leaves your computer.
* **Microphone Selection Dropdown:** Dynamically cycle through and switch your active audio devices right from the user interface.
* **Smart Sample Rate Detection:** Auto-calibrates the voice recognition engine to match your mic's hardware frequency (e.g., 16000Hz, 44100Hz, 48000Hz).
* **Asynchronous Queue Pipeline:** Multi-threaded architecture prevents lag and UI freezing during intense gameplay.
* **No Audio Out Interruption:** Pure Speech-to-Text translation mode—keeps your standard microphone line entirely open for normal VRChat voice chat.

---

## Quick Start (For Users)

If you are using the pre-compiled **`SST.VRChat.exe`**, setting it up is incredibly easy:

1. Launch **VRChat**.
2. Open your VRChat Action Menu (Expressions Wheel), navigate to **Options** -> **OSC**, and ensure **OSC is Enabled**.
3. Launch **`SST.VRChat.exe`**.
4. Select your preferred microphone from the drop-down menu.
5. Click **Start Listening** and begin speaking! Your text will automatically pipe straight into your in-game chatbox.

*Note: Since the voice patterns are packed directly inside the executable, you do not need to download external data zips or dependencies to run the `.exe` file.*

---

## For Developers & Manual Execution

If you want to run or modify the raw Python source code (`SST.VRChat.py`), follow these steps:

### 1. Prerequisites & Dependencies
Make sure you have Python 3.10+ installed. Install the required system modules via your command prompt:

```bash
pip install vosk python-osc sounddevice tkinter
