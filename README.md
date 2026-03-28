# VegiAttacker 🥕🎯

A WebRTC-based remote control system for a vegetable-targeting device. Control your robot or vehicle from a browser to hunt down vegetables!

## Overview

VegiAttacker is a fun IoT/robotics project that lets you control a device (like a small rover or a targeting mechanism) over the web using WebRTC for real-time communication. The system consists of:

- A **controller interface** (`controller.html`) for steering or targeting.
- A **device interface** (`index.html`) running on the target device (e.g., Raspberry Pi, smartphone) that receives commands.

The project is currently under active development, with recent updates focusing on WebRTC integration.

## Features

- 🌐 **Browser-based control** – No app installation needed.
- ⚡ **Real-time communication** using WebRTC for low-latency commands.
- 🎮 **Intuitive interface** – designed for easy operation.
- 🧩 **Modular architecture** – easily extendable for different hardware.

## Project Structure

```
vegiattacker/
├── index.html          # Device-side interface (receives commands)
├── controller.html     # Controller interface (sends commands)
└── README.md           # This file
```

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge)
- Two devices on the same network (or with accessible IPs) for testing
- For full functionality, a WebRTC signaling server (you can use a simple Node.js server or a public signaling service)

### Running Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/athishsreeram/vegiattacker.git
   cd vegiattacker
   ```
2. Host the files using a local web server (e.g., with Python):
   ```bash
   # Python 3
   python -m http.server 8000
   ```
3. Open `index.html` on the device you want to control (e.g., a robot) and `controller.html` on your controlling device.
4. Establish a WebRTC connection between them (implementation details to be added – currently expects a signaling mechanism).

### Next Steps for Full Implementation
To make the project fully functional, you need to:
- Set up a signaling server to exchange WebRTC offers/answers.
- Implement the control logic in `controller.html` to send commands (e.g., over a data channel).
- Write the device-side code in `index.html` to act on received commands (e.g., move motors, trigger a camera).

## Future Plans

- Add a signaling server example.
- Integrate with common robotics platforms (Arduino, Raspberry Pi).
- Add video streaming from the device.
- Create a more polished UI.

## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests with improvements, bug fixes, or new features.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Acknowledgments

- Built with WebRTC for real-time communication.
- Inspired by playful robotics projects.
