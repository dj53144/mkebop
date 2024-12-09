# mkebop
An advanced karaoke system using a Raspberry Pi Zero 2 W to send backing sound to a DAC and broadcast a lyrics WAV file to Bluetooth glasses.
# Advanced Multi-Channel Karaoke System

## Overview
The Advanced Multi-Channel Karaoke System is designed to deliver a rich karaoke experience on the Raspberry Pi Zero 2 W. It integrates multi-channel audio output, a Python GUI for configuration, and hardware controls using a display with three buttons and a joystick. The system also supports Bluetooth keyboards for enhanced usability.

---

## Features
- **Multi-Channel Audio Output**: Configurable audio routing for multiple speakers and microphones.
- **Python GUI**: Intuitive interface for system configuration and song management.
- **Hardware Controls**: Navigate menus and adjust settings using three buttons and a joystick on the display.
- **Bluetooth Keyboard Support**: Input song lyrics, control playback, and more with ease.
- **Lightweight Design**: Optimized for the Raspberry Pi OS Lite.

---

## Hardware Requirements
- **Raspberry Pi Zero 2 W**
- **1.3-inch IPS LCD Display HAT** (240x240 pixels, SPI interface, ST7789 driver)
- **Three Buttons and Joystick** (integrated with the display HAT)
- **Bluetooth Keyboard**
- **Multi-Channel USB Audio Interface**
- **Speakers and Microphones**
- **MicroSD Card (32GB or higher)** with Raspberry Pi OS Lite

---

## Software Components
### Core Functionality
1. **Python GUI**:
   - Designed using `Tkinter` or `PyQt5`.
   - Displays menus for:
     - System configuration (audio channels, display settings).
     - Song selection and playback control.
     - User profiles and preferences.
   - Supports navigation via buttons, joystick, and keyboard.
   
2. **Audio Management**:
   - Powered by `alsa-utils` and `pulseaudio`.
   - Allows independent routing of audio channels for karaoke music, vocals, and effects.
   - Integration with UHC filters for audio clarity in noisy environments.

3. **Bluetooth Integration**:
   - Handles Bluetooth keyboard pairing and input management.
   - Configurable shortcuts for playback control, lyric scrolling, and system commands.

4. **Button and Joystick Control**:
   - Configured to work with the display HAT.
   - Default mappings:
     - Joystick: Navigate menus.
     - Buttons: Select, Back, and Power options.

5. **Song Library**:
   - Supports playback of `.mp3`, `.wav`, and `.kar` files.
   - Displays synced lyrics during playback (when available).
   - Organized into playlists and searchable by title or artist.

---

## Software Installation
1. **Update System**:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Install Dependencies**:
   ```bash
   sudo apt install -y python3 python3-pip git alsa-utils pulseaudio vlc
   sudo pip3 install pillow pyalsaaudio
   ```

3. **Clone the Repository**:
   ```bash
   git clone https://github.com/dj53144/mkebop.git
   cd mkebop
   ```

4. **Run the Application**:
   ```bash
   python3 mkebop_gui.py
   ```

---

## System Configuration
### Audio
- Configure multi-channel audio in the GUI under **Settings > Audio Configuration**.
- `.asoundrc` file is automatically generated based on user preferences.

### Display
- GUI scales to fit the 240x240 resolution of the IPS LCD Display.
- Brightness and rotation can be adjusted in **Settings > Display Options**.

### Buttons and Joystick
- Default mappings can be customized in the GUI under **Settings > Input Configuration**.

---

## Future Enhancements
- **Cloud Integration**: Sync playlists and song libraries across devices.
- **Voice Effects**: Add reverb, pitch correction, and echo for vocals.
- **Live Streaming**: Broadcast karaoke sessions via platforms like YouTube or Twitch.

---

## Contributing
We welcome contributions! If you’d like to add features, improve performance, or fix bugs, please fork the repository and submit a pull request.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
